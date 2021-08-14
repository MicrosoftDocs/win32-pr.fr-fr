---
title: Outil du compilateur de service Web
description: Pour prendre en charge le modèle de service, wsutil.exe génère un en-tête à utiliser à la fois côté client et côté service. Il génère un fichier proxy C pour le côté client et un fichier stub C pour le côté service, si nécessaire.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Services Web de l’outil du compilateur de service Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92e1195cd9d3a8e8d9fa1b7be94421d68f3cbdf2242be6fa0d05be5cc3c743f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962838"
---
# <a name="web-service-compiler-tool"></a>Outil du compilateur de service Web

Pour prendre en charge le modèle de service, wsutil.exe génère un en-tête à utiliser à la fois côté client et côté service. Il génère un fichier proxy C pour le côté client et un fichier stub C pour le côté service, si nécessaire.


Pour prendre en charge la [sérialisation](serialization.md), le compilateur génère des en-têtes pour les descriptions d’éléments pour les définitions d’éléments globaux et toutes les informations de définition de type dans le fichier proxy à consommer par le moteur de sérialisation.

Usage

**Commutateur de commutateurs de \[ ligne de commandeWsUtil.exe \[ -options \] :\]<filename>**

commutateurs de ligne de commande

Spécifie WsUtil.exe options du compilateur. Les commutateurs peuvent apparaître dans n’importe quel ordre. Les tirets (« - ») et les barres obliques (« / ») sont traités comme les mêmes.

Liste des options de ligne de commande

-   @filename Spécifie que le fichier d’entrée doit être traité comme un fichier réponse. Cette option peut être utilisée plusieurs fois, à n’importe quel endroit de la liste d’arguments.
-   /wsdl : <filename> : <\_ url facultative> spécifie que le fichier d’entrée doit être traité en tant que fichier WSDL. Plusieurs entrées WSDL sont autorisées et tous les fichiers WSDL spécifiés sont traités. L' \_ URL facultative spécifie l’emplacement à partir duquel les métadonnées ont été récupérées. Si aucune \_ URL facultative n’est spécifiée, Wsutil génère une URL unique en interne. Voir aussi [prise en charge des stratégies](policy-support.md).
-   /xsd : <filename> spécifie que le nom de fichier d’entrée doit être traité comme un fichier de schéma. Plusieurs entrées XSD sont autorisées et tous les fichiers de schéma spécifiés sont traités.
-   /wsp : <filename> : <\_ url facultative> spécifie que le nom de fichier d’entrée doit être traité en tant que métadonnées de stratégie. Plusieurs entrées wsp sont autorisées et tous les fichiers de stratégie spécifiés sont traités. L' \_ URL facultative spécifie l’emplacement à partir duquel les métadonnées ont été récupérées. Si aucune \_ URL facultative n’est spécifiée, Wsutil génère une URL unique en interne. Les fichiers de stratégie sont ignorés si l’indicateur/nopolicy est spécifié. Voir aussi [prise en charge des stratégies](policy-support.md).
-   /nopolicy désactive le traitement de la stratégie.
-   /out : <dirname> spécifie le nom du répertoire pour les fichiers de sortie
-   /NoClient ne pas générer le stub côté client.
-   /noservice ne pas générer le stub côté service.
-   /Prefix : <string> ajoute la chaîne spécifiée à tous les identificateurs générés.
-   /FullName ajoute un nom de fichier normalisé aux identificateurs générés. Par défaut, seul le nom spécifié dans l’attribut « Name » est utilisé pour générer des identificateurs pour les descriptions associées.
-   /String : <WS \_ string>\|<WCHAR \*> par défaut, Wsutil génère WCHAR \* pour le type xsd : String. L’application peut utiliser cet indicateur pour remplacer ce comportement et génère à la \_ place WS String pour xsd : type.
-   /help afficher le message d’aide
-   /? Identique à/help
-   /W : x options de gestion des erreurs. Peut être W :0-W : 4 \| WX
-   /nologo ne pas générer d’informations spécifiques au compilateur sur la sortie de la console.
-   les/nostamp ne génèrent pas d’informations spécifiques au compilateur sur les fichiers générés.

Par défaut, le compilateur génère les fichiers suivants pour le fichier WSDL, ou WSDL retourné à partir de l’échange de métadonnées :

-   Proxy client ({InputFileName}. c)
-   Service stub ({InputFileName}. c)
-   Fichier d’en-tête ({InputFileName}. h)

    La racine du nom de fichier généré est le nom du fichier d’entrée. Les extensions de fichier d’entrée d’origine sont conservées pour empêcher la collision de nom de fichier pour les fichiers générés. Par défaut, les stubs de client et de service sont générés dans le même fichier, avec le code stub de service généré après le code proxy.

    Par défaut, le compilateur génère les fichiers suivants pour un fichier XSD pour le schéma retourné par l’échange de métadonnées :

-   descriptions de sérialisation ({InputFileName}. c)
-   Fichier d’en-tête ({InputFileName}. h)

    La racine du nom de fichier est le nom du service.

Wsutil.exe génère une section « tampon » au début de tous les fichiers générés, indiquant l’option de compilateur, la version de l’outil, l’option de ligne de commande applicable, etc. Cette section peut être désactivée à l’aide de l’option/nostamp pour éviter le bruit lors de la comparaison des fichiers générés.

Wsutil ne prend pas en charge le téléchargement de métadonnées

Le compilateur Wsutil fonctionne uniquement à partir du fichier de métadonnées local. L’outil ne prend pas en charge le téléchargement de métadonnées à partir de services Web en cours d’exécution. Les développeurs peuvent utiliser d’autres outils de service Web pris en charge, tels que Svcutil, pour télécharger des métadonnées sur l’ordinateur local, inspecter les fichiers enregistrés et transmettre ces fichiers à wsutil.exe pour la compilation.

Prise en charge de plusieurs fichiers d’entrée/sortie

Le schéma WSDL et XML permet d’inclure ou d’importer des définitions d’autres espaces de noms spécifiés dans d’autres emplacements/fichiers. Wsutil prend en charge plusieurs entrées de schéma/WSDL/de stratégie et génère un jeu d’en-tête/stub pour chaque fichier d’entrée. Wsutil ne suit pas les instructions include et import. Au lieu de cela, l’application doit transmettre des fichiers contenant tous les espaces de noms nécessaires à Wsutil afin que l’outil puisse résoudre toutes les dépendances lors de la compilation.

**WsUtil.exe/xsd : StockQuote. xsd/wsdl : StockQuote. wsdl/wsdl : StockQuoteService. wsdl**

Wsutil génère trois ensembles de fichiers de sortie :

-   StockQuote. xsd. c StockQuote. xsd. h
-   StockQuote. wsdl. c StockQuote. wsdl. h
-   StockQuoteService. wsdl. h stockquoteservices. wsdl. c

Format des fichiers de sortie

Pour chaque fichier de sortie, Wsutil génère des définitions disponibles en externe dans le fichier d’en-tête. Outre les définitions de structure C et les prototypes de fonction stub, toutes les autres définitions associées aux services Web sont encapsulées dans une structure globale nommée avec un nom de fichier normalisé.

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

Notez que tous les champs ne sont pas générés pour la structure globale. Un champ de niveau supérieur est généré uniquement lorsque les définitions associées sont spécifiées dans le fichier d’entrée. Par exemple, aucun champ de message, d’opération et de contrat n’est généré pour les fichiers XSD.

Niveaux d’avertissement et niveau d’erreur

Comme pour le compilateur C, WsUtil.exe prend en charge quatre niveaux d’avertissement et un niveau d’erreur :

-   WsUtil.exe génère des erreurs avec des échecs irrécupérables, comme un fichier WSDL non valide, des options de compilateur non valides, etc.
-   WsUtil génère des avertissements W1 avec des problèmes récupérables graves. Le compilateur peut passer à, mais l’utilisateur doit être conscient du problème. Par exemple, un avertissement W1 est généré s’il existe des attributs non pris en charge, tels que des facettes WSDL, en WSDL qui n’affectent pas la génération de code.
-   WsUtil génère des avertissements W2 avec des problèmes moins graves. Il n’y a aucune perte de fonctionnalité, mais le développeur d’applications peut souhaiter le savoir. Comme les comportements qui peuvent être différents des autres plateformes.
-   WsUtil génère des avertissements W3 avec un impact minimal sur le code généré. Par exemple, wsutil.exe génère un avertissement W3 quand une chaîne normalisée est différente de la chaîne d’origine.
-   L’avertissement W4 ressemble davantage à des avertissements « informatifs » et WsUtil à un problème de type W4 dans des cas comme l’ignorance de l’attribut de documentation dans WSDL.
-   WX indique que le compilateur traite l’avertissement comme une erreur. Par exemple, Wsutil génère une erreur pour tous les avertissements W1 si/W : 1/WX est spécifié.

/W : {N} spécifiez le niveau de message d’avertissement qui doit être généré. /W : 1 signifie que les avertissements de niveau 1 doivent être générés et que les avertissements de niveau 2 et inférieur doivent être masqués et non générés par l’outil.

## <a name="fullname"></a>/fullname

Cette option indique que WsUtil.exe génère un nom complet pour les identificateurs afin d’éviter une éventuelle collision de noms. Par exemple, dans l’exemple. xsd, nous avons :

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

Par défaut WsUtil.exe génère :

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Toutefois, si l’option de ligne de commande/FullName est spécifiée, WsUtil.exe génère la définition de structure suivante à la place :

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalisation

L’outil est indépendant de la langue et peut être localisé dans différentes langues. Tous les messages d’erreur/la sortie de la console peuvent être localisés. Toutefois, les options de ligne de commande restent en anglais.

## <a name="environment-variable"></a>Variable d’environnement

WsUtil.exe n’utilise pas de variables d’environnement.

## <a name="platform-independent"></a>Indépendant de la plateforme

Les fichiers de sortie de WsUtil.exe sont indépendants de la plateforme. Aucun code dépendant de l’architecture n’est généré dans le stub ; tout ce qui est spécifique à l’architecture est pris en charge par le compilateur C. Le stub peut être utilisé dans toutes les plateformes que nous prenons en charge.

Pour obtenir une description de wsutil.exe, consultez la section prise en charge de [WSDL](wsdl-support.md) et du [support de schéma](schema-support.md) .

 

 




