# php_Project
php

25 ans de vie
niveau de fiabilité elevé
php est un language est ecrit en c
language interpreté;

serveur : Apache


sudo apt-get install php libapache2-mod-php

sudo chmod 755 -R ../../var/www/html/monsite/ 
sudo chown francisco:francisco -R monsite 
sudo systemctl restart apache2 

echo pour l'affichage


<?= "bonjour" ?> on l'utilise souvent quand on melange du php avec l'html

print ~≳ echo
ex: print "ok";


## VARIABLE ET TYPE

-boolean ou bool;
-integer ou int;
-float ou double;
-string;

4 types composés

-array;
-object;

## function en php

intdiv();
fmod();

$number = 16;
echo gettype($number);
echo 'j'ai '.$number.'ans';
<=> -(0 si c'est égal)
    -(-1 si c'est inferieur)
    -(1si c'est superieur)

# Verifier lexistance dune variable;

unset($mavariable) : pour dire que la variable n'existe pas;

isset($mavariable) : pour dire que la variable exite;

is_int();

function ma_fonct(...$lotOfVariables)
{
    foreach($lotOfVariables as $data)
    var_dump($lotOfVariables)
}

$v = ma_fonctio()
{

};

v();

$tab_integers = arrays();// tableau vide;

$tab_integers = [
    10,11,12,13,14
];

var_dump($tab_integers);

echo '<pres>';
print_r($tab_integers);
echo '</pres>';

$hbts = [
    "paris" => 1200,
    "toulouse" => 90,
    "bercy" => 160
];

foreach($tab_population_villes as $k => $v)
    echo '<p>'.$k.'/'.$v.'</p>';

Fonctions usuelles pour les tableaux 👍

> array_push()
> arrqy_pop() ou array_shift()
> in_array()


# GESTION D'ERREURS


error_reporting(-1);
ini_set("display_errors", 1);

function my_error_handler()
{
    
}
set_error_handlers($my_error_handler);

$my_error_handler = function ()
{

};

set_error_handler($my_error_handler);

/*
function error_handler($errno, $errmsg, $errfile, int $errline, array $errdatas)
E_USER_ERROR | E_USER_WARNIG | E_USER_NOTICE
*/

$my_error_handler = function(int $errno, string $errmsg,string $errfile, int $errline)
{
    switch($errno)
    {
        case E_USER_ERROR:
            echo $errmsg;
            break;

        case E_USER_WARNING:
            echo $errmsg.' sur le fichier '.$errfile;
            break;

        case E_USER_NOTICE:
            echo $errmsg;
            break;

        default:
            echo 'ERREUR' : '.$errmsg;
            break;
    }
};

set_error_handler($my_error_handler);
