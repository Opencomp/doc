# Présentation de l'API REST

## Qu'est-ce-qu'une API REST ?

> **REST** \(**representational state transfer**\) est un style d'[architecture logicielle](https://fr.wikipedia.org/wiki/Architecture_informatique) définissant un ensemble de contraintes à utiliser pour créer des services web. Les services web conformes au style d'architecture REST, aussi appelés services web **RESTful**, établissent une interopérabilité entre les ordinateurs sur [Internet](https://fr.wikipedia.org/wiki/Internet). Les services web REST permettent aux systèmes effectuant des requêtes de manipuler des ressources web via leurs représentations textuelles à travers un ensemble d'opérations uniformes et prédéfinies [sans état](https://fr.wikipedia.org/wiki/Protocole_sans_%C3%A9tat). 
>
> _—_ [_Contributeurs de Wikipédia_](https://xtools.wmflabs.org/articleinfo/fr.wikipedia.org/Representational_state_transfer?editorlimit=200)_, l'encyclopédie libre et gratuite_

## Intérêt de l'API REST ?

L'API REST d'Opencomp vous permet d'effectuer des actions automatisées sans avoir besoin d'utiliser manuellement l'application \(par l'entremise d'un navigateur Web\).

L'API peut, par exemple, permettre à un programme de récupérer des données depuis Opencomp \(par exemple les élèves de vos classes, vos évaluations, etc.\) mais également d'en envoyer \(résultats obtenus aux évaluations par exemple\).

## Authentification

L'API REST est sécurisée et vous n'avez bien sûr accès qu'aux données concernant vos classes.

Afin de vous authentifier, vous devez passer le paramètre d'URL **`api_key`** avec pour valeur votre clé d'API personnelle accessible depuis la rubrique **Mon compte** de l'application.

## Formats de retour

Le format de retour est toujours spécifié en fin d'URL.

_Les formats de retour possibles sont :_

### JSON

> **JavaScript Object Notation** \(**JSON**\) est un [format de données](https://fr.wikipedia.org/wiki/Format_de_donn%C3%A9es) textuelles dérivé de la notation des [objets](https://fr.wikipedia.org/wiki/Objet_%28informatique%29) du langage [JavaScript](https://fr.wikipedia.org/wiki/JavaScript). Il permet de représenter de l’information structurée.
>
> Un document JSON a pour fonction de représenter de l'information accompagnée d'étiquettes permettant d'en interpréter les divers éléments, sans aucune restriction sur le nombre de celles-ci.
>
> Un document JSON ne comprend que deux types d'éléments structurels :
>
> * des ensembles de paires « nom » \(alias « clé »\) / « valeur » ;
> * des listes ordonnées de valeurs.
>
> Ces mêmes éléments représentent trois types de données :
>
> * des objets ;
> * des tableaux ;
> * des valeurs génériques de type [tableau](https://fr.wikipedia.org/wiki/Tableau_%28structure_de_donn%C3%A9es%29), [objet](https://fr.wikipedia.org/wiki/Objet_%28informatique%29), [booléen](https://fr.wikipedia.org/wiki/Bool%C3%A9en), nombre, [chaîne](https://fr.wikipedia.org/wiki/Cha%C3%AEne_de_caract%C3%A8res) ou [null](https://fr.wikipedia.org/wiki/Null).
>
> _—_ [_Contributeurs de Wikipédia_](https://xtools.wmflabs.org/articleinfo/fr.wikipedia.org/JavaScript_Object_Notation?editorlimit=200#top-editors)_, l'encyclopédie libre et gratuite_

### XML

> L'**Extensible Markup Language**, généralement appelé **XML**, « langage de balisage extensible » en français, est un [métalangage](https://fr.wikipedia.org/wiki/M%C3%A9talangage) informatique de [balisage](https://fr.wikipedia.org/wiki/Langage_de_balisage) générique qui dérive du [SGML](https://fr.wikipedia.org/wiki/SGML). Sa syntaxe est dite « extensible » car elle permet de définir différents [espaces de noms](https://fr.wikipedia.org/wiki/Espace_de_noms_XML), c'est-à-dire des langages avec chacun leur vocabulaire et leur grammaire, comme [XHTML](https://fr.wikipedia.org/wiki/XHTML), [XSLT](https://fr.wikipedia.org/wiki/XSLT), [RSS](https://fr.wikipedia.org/wiki/RSS), [SVG](https://fr.wikipedia.org/wiki/SVG)… Elle est reconnaissable par son usage des [chevrons](https://fr.wikipedia.org/wiki/Chevron_%28typographie%29) \(`<`, `>`\) encadrant les noms des balises. L'objectif initial de XML est de faciliter l'échange automatisé de contenus complexes \([arbres](https://fr.wikipedia.org/wiki/Arbre_enracin%C3%A9), texte enrichi, etc.\) entre [systèmes d'informations](https://fr.wikipedia.org/wiki/Syst%C3%A8me_d%27information) hétérogènes \([interopérabilité](https://fr.wikipedia.org/wiki/Interop%C3%A9rabilit%C3%A9_en_informatique)\).
>
> _—_ [_Contributeurs de Wikipédia,_](https://xtools.wmflabs.org/articleinfo/fr.wikipedia.org/Extensible_Markup_Language?editorlimit=2000#top-editors) _l'encyclopédie libre et gratuite_

## Pagination des résultats

Lorsque l'API REST renvoie un ensemble de résultats \(listing\), les résultats sont paginés. Dans ce cas, les informations de pagination telles que le nombre total de résultats, le nombre de résultats par page et la quantité de pages sont indiqués dans le tableau portant la clé `paging`.

{% tabs %}
{% tab title="Exemple JSON" %}
```javascript
{
     "paging": {
         "count":38916,
         "perPage":30,
         "pageCount":1298
     },
     "objects": [{...},{...},{...}, ...]
 }
```
{% endtab %}

{% tab title="Exemple XML" %}
```markup
<response>
    <paging>
        <count>38916</count>
        <perPage>30</perPage>
        <pageCount>1298</pageCount>
    </paging>
    <objects>...</objects>
    <objects>...</objects>
    <objects>...</objects>
</response>
```
{% endtab %}
{% endtabs %}

## Points de terminaison

{% page-ref page="points-de-terminaison/api-rest-nomenclatures.md" %}

{% page-ref page="points-de-terminaison/api-rest.md" %}

