---
title: Identificateurs de propriété réservés
description: Les identificateurs de propriété réservés ne peuvent pas être utilisés en tant qu’identificateurs de propriété (ID). Tout identificateur de propriété (ID) peut être utilisé sauf 0, 1 et toute valeur supérieure ou égale à 0x80000000. Ces valeurs d’identificateur de propriété sont réservées à une utilisation par les applications.
ms.assetid: d313a7b1-4cac-41f8-ba38-bf9cfaeb9d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a16a8e232a31864a402b01033a829183105905c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463230"
---
# <a name="reserved-property-identifiers"></a>Identificateurs de propriété réservés

Les identificateurs de propriété réservés ne peuvent pas être utilisés en tant qu’identificateurs de propriété (ID). Tout identificateur de propriété (ID) peut être utilisé sauf 0, 1 et toute valeur supérieure ou égale à 0x80000000. Ces valeurs d’identificateur de propriété sont réservées à une utilisation par les applications.

Le tableau suivant répertorie les ID de propriété réservés et la description de ce à quoi l’ID de propriété est réservé.



| ID de propriété réservée | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                    | Réservé à la création d’un [dictionnaire de nom complet de jeu de propriétés](property-set-display-name-dictionary.md)facultatif. Cela permet aux utilisateurs de jeux de propriétés d’attacher la signification aux propriétés, au-delà de celles fournies par l’indicateur de type.                                                                                                                                                                                                                                                                                                                                                                |
| 1                    | Réservé en tant qu’indicateur de la page de codes (Windows) ou du script (Macintosh) à utiliser lors de l’interprétation des chaînes dans le jeu de propriétés.<br/> Toutes les valeurs de chaîne dans le jeu de propriétés doivent être stockées avec la même page de codes. La valeur du système d’exploitation d’origine dans l’en-tête du jeu de propriétés (PROPERTYSETHEADER ::d wOSVer) détermine si l’indicateur de page de codes correspond à une page de codes Windows ou à un script Macintosh.<br/>                                                                                                                                                        |
| 0x80000000           | Réservé comme indication des paramètres régionaux pour lesquels le jeu de propriétés est écrit.<br/> Les paramètres régionaux par défaut d’un jeu de propriétés sont les paramètres régionaux par défaut du système (paramètres régionaux \_ \_ par défaut du système). Pour plus d’informations sur les paramètres régionaux \_ \_ par défaut du système, consultez les API Win32. La valeur par défaut est utilisée dans le cas où l’indicateur de paramètres régionaux n’existe pas dans le jeu de propriétés.<br/>                                                                                                                                                                                                                        |
| 0x80000003           | Réservé en tant qu’indicateur de comportements de jeu de propriétés. Cette valeur d’ID de propriété est un \_ UI4 VT et commence par un type de données **DWORD** contenant la valeur VT \_ Ui4 suivi d’un **DWORD** indiquant le comportement du jeu de propriétés.<br/> Actuellement, le seul bit de cette valeur défini est le bit de poids faible (0x1). Si ce bit est défini, il indique que les noms de jeux de propriétés, indiqués par l’ID de propriété 0, doivent être considérés comme sensibles à la casse. Si ce bit n’est pas défini ou si la propriété Behavior (ID 0x80000003) n’existe pas, les noms doivent être considérés comme non sensibles à la casse.<br/> |
| Égale           | Réservé à la commodité de la programmabilité. Elle ne doit jamais apparaître dans un jeu de propriétés sérialisé.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Les identificateurs de propriété avec l’ensemble de bits élevé (c’est-à-dire les valeurs négatives) sont réservés pour une utilisation ultérieure par Microsoft.

Parmi les propriétés réservées, celles dont les valeurs d’ID sont comprises dans la plage 0x80000000 à 0xBFFFFFFF sont considérées comme étant en lecture seule par des implémentations qui ne comprennent pas leur signification. Par exemple, si une implémentation ne comprend pas la signification de la propriété 0x80000000, elle doit autoriser la lecture, mais pas l’écriture ou la suppression de cette propriété. Une telle implémentation doit permettre de lire, d’écrire ou de supprimer une propriété de la plage 0xC0000000 à 0xFFFFFFFE. L’ID de propriété 0xFFFFFFFF est une valeur réservée et ne doit jamais apparaître dans un jeu de propriétés sérialisé.

## <a name="property-set-locale"></a>Paramètres régionaux du jeu de propriétés

Les applications peuvent choisir de prendre en charge les paramètres régionaux ou d’utiliser le comportement par défaut. Il est recommandé que les applications autorisent les utilisateurs à spécifier des paramètres régionaux de travail. De telles applications doivent écrire l’identificateur de paramètres régionaux spécifié par l’utilisateur dans la propriété. Les applications qui utilisent les paramètres régionaux par défaut de l’utilisateur (paramètres régionaux \_ \_ par défaut de l’utilisateur) doivent écrire l’identificateur de paramètres régionaux par défaut de l’utilisateur dans la propriété. Pour plus d’informations sur les paramètres régionaux \_ \_ par défaut de l’utilisateur, consultez l’API Win32.

> [!Note]  
> Si l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) est utilisée pour créer un jeu de propriétés, les paramètres régionaux par défaut de l’utilisateur sont automatiquement écrits comme indicateur de paramètres régionaux.

 

Les applications doivent également gérer le cas d’un objet étranger, qui est un emplacement où les paramètres régionaux ne sont pas les paramètres régionaux de l’application, les paramètres régionaux de l’utilisateur ou les paramètres régionaux système.

La propriété de l’indicateur de paramètres régionaux est de type VT \_ U14 et, par conséquent, se compose d’une **valeur DWORD** qui contient VT \_ U14, suivie d’une **valeur DWORD** contenant l’identificateur de paramètres régionaux (LCID), tel que défini dans l’API Win32.

## <a name="code-page-indicator"></a>Indicateur de page de codes

Lorsqu’une application qui n’est pas l’auteur d’un jeu de propriétés modifie une propriété de type chaîne dans le jeu, elle doit examiner l’indicateur de page de codes et effectuer l’une des actions suivantes :

-   Écrit la chaîne au format spécifié par l’indicateur de page de codes.
-   Remplacez et réécrivez pour modifier la page de codes.

Si une application ne peut pas reconnaître cet indicateur, elle ne doit pas modifier la propriété. Tous les créateurs de jeux de propriétés doivent écrire un indicateur de page de codes ; Toutefois, si l’indicateur de page de codes n’est pas présent, la page de codes en vigueur sur l’ordinateur du lecteur doit être prise en supposer.

> [!Note]  
> Si l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) est utilisée pour créer un jeu de propriétés, l’indicateur de page de codes est automatiquement écrit.

 

Les valeurs possibles pour la page de codes sont fournies dans l’API Win32 (pour plus d’informations, consultez la fonction [**GetACP**](/windows/desktop/api/winnls/nf-winnls-getacp) ) et *à l’intérieur du volume Macintosh VI*, pages 14-111. (Ces ressources peuvent ne pas être disponibles dans certaines langues et certains pays.) Par exemple, la page de codes US ANSI est représentée par 0x04E4 (1252 au format décimal), tandis que la page de codes Unicode est 0x04B0 (1200 en décimal).

Il est recommandé d’utiliser la page de codes Unicode lorsque cela est possible, et \_ d’utiliser VT LPWStr au lieu de VT \_ LPSTR pour éviter les conversions Unicode multioctets < > pendant le stockage et la récupération. L’utilisation de la même page de codes pour tous les jeux de propriétés est la seule façon d’obtenir des jeux de propriétés interopérables sur une base mondiale. Dans la page de codes Unicode ou non-Unicode, sachez que le nombre au début d’une VT de VT \_ ou VT \_ est un nombre d' **octets** et non un nombre de **caractères** . Ce nombre d’octets comprend un ou deux octets nuls à la fin de la chaîne (terminateur **null** de la chaîne).

L’ID de propriété 1 est un \_ type VT I2 et commence par une valeur **DWORD** qui contient la valeur VT \_ I2, suivie d’un **short** qui indique la page de codes.

 

