---
description: Préparation d’un fichier de configuration de ressource
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Préparation d’un fichier de configuration de ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112810"
---
# <a name="preparing-a-resource-configuration-file"></a>Préparation d’un fichier de configuration de ressource

Les utilitaires du compilateur MUIRCT et RC décrits dans [utilitaires de ressources](resource-utilities.md) fournissent une option de ligne de commande qui vous permet de spécifier un fichier de configuration de ressources pour les ressources de langue de base. L’utilisation de ce fichier XML public et explicite permet de mieux contrôler le fractionnement des ressources que ce qui peut être obtenu à l’aide des commutateurs de ligne de commande standard des utilitaires. Toutefois, même si vous ne fournissez pas de fichier de configuration de ressources comme entrée, les fichiers de ressources de la LN et spécifiques à la langue contiennent des données de configuration de ressource.

Tous les fichiers de configuration de ressources pour les applications Win32 commencent et se terminent de la même manière :


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Cette rubrique se concentre sur les aspects du schéma XML qui sont utiles lors de la création de code non managé sur Windows Vista et versions ultérieures. En particulier, il est uniquement concerné par le comportement de l’élément win32Resources.

## <a name="win32resources-element"></a>Élément win32Resources

L’élément win32Resources a les attributs décrits dans le tableau suivant.



| Nom de l’attribut           | Obligatoire | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | Non        | Type de fichier. Doit toujours être « application ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| somme de contrôle                 | Non        | Valeur de somme de contrôle à afficher dans les données de configuration de ressource du fichier LN et des fichiers de ressources spécifiques à une langue. Par exemple, cet attribut vous permet de copier la somme de contrôle à partir d’un seul fichier de ressources spécifique à une langue, en le comparant à celle de l’anglais (États-Unis), et de placer la somme de contrôle dans un fichier de ressources spécifique à une langue. La somme de contrôle peut être spécifiée sous la forme d’une chaîne de nombres hexadécimaux ne dépassant pas 32 caractères. La valeur numérique doit être contenance dans un nombre de 128 bits. |
| langage                 | Non        | Langue spécifiée à l’aide d’un format de nom conforme à la norme RFC 4646 (Windows Vista et versions ultérieures), par exemple, en-US pour l’anglais (États-Unis).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | Non        | Langue à insérer dans les données de configuration de ressource pour le fichier LN, représentant le langage de secours ultime à utiliser dans une recherche de fichier de ressources spécifique à une langue correspondante. Si le chargeur de ressources ne parvient pas à charger un fichier de ressources demandé à partir des langues d’interface utilisateur préférées du thread, il utilise un langage de secours ultime comme dernière tentative. Le langage est spécifié à l’aide d’un format de nom conforme à la norme RFC 4646 (Windows Vista et versions ultérieures), par exemple, en-US pour l’anglais (États-Unis).       |
| ultimateFallbackLocation | Non        | Emplacement de secours. Spécifiez « Internal » si les ressources de secours ultimes sont compilées dans le fichier LN. Spécifiez « External » (valeur par défaut) si le fichier LN doit faire référence à un fichier de ressources spécifique à une langue pour ses ressources de secours ultimes.                                                                                                                                                                                                                                                                                |



 

Dans le fichier de configuration de ressource, l’élément win32Resources contient les sous-éléments décrits dans le tableau suivant.



| Nom de l’élément       | Description                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Ressources qui encapsulent des informations sur les types de ressources et les ressources individuelles contenues dans un fichier de ressources spécifique à une langue. |
| neutralResources   | Ressources qui encapsulent des informations sur les types de ressources contenus dans un fichier LN.                                                 |



 

## <a name="localizedresources-element"></a>Élément localizedResources

Élément des ressources localisées. Par défaut, cet élément n’a pas d’attributs et un seul type de sous-élément. Il s’agit simplement d’un conteneur pour les éléments resourceType.



| Nom d’attribut | Description                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Type d’une ressource individuelle contenue dans un fichier de ressources spécifique à une langue. |



 

## <a name="neutralresources-element"></a>Élément neutralResources

Élément ressources neutres. Cet élément est simplement un conteneur pour les éléments resourceType.



| Nom d’attribut | Description                                        |
|----------------|----------------------------------------------------|
| resourceType   | Type d’une ressource unique contenue dans un fichier LN. |



 

## <a name="resourcetype-element"></a>resourceType, élément

L’élément resourceType encapsule des informations sur un type de ressource unique ou une ressource individuelle. Il possède les attributs indiqués ci-dessous.

> [!Caution]  
> Certains défauts de configuration des ressources sont interceptés uniquement par le compilateur RC ou MUIRCT, selon le fichier de ressources d’entrée ou le contenu du fichier binaire. Les erreurs resourceType dans le fichier de configuration de ressource qui n’existent pas dans le fichier d’entrée ne sont pas interceptées, ce qui entraîne un comportement inattendu. Les utilisateurs peuvent utiliser un fichier de configuration de ressource défectueux et ne savent pas jusqu’à ce qu’ils introduisent des fichiers binaires qui utilisent les parties cassées du fichier de configuration de ressources, ce qui crée l’apparence des arrêts des fichiers binaires actuels.

 



| Nom de l’attribut | Obligatoire | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Oui       | Nom de type ou identificateur de la ressource. Spécifiez un nom de chaîne ou un nombre. Si vous utilisez un nombre, faites précéder la chaîne d’un « \# » pour indiquer qu’elle représente un nombre. Chaque élément resourceType ne doit avoir qu’un seul attribut *typeNameId* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | Non        | Chaîne de nom d’élément de la ressource, à placer dans le fichier de ressources spécifique à la langue. Vous pouvez spécifier plusieurs noms, séparés par des espaces blancs, par exemple, « HTML MOFDATA ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | Non        | Identificateur d’un élément de ressource individuel à placer dans le fichier de ressources spécifique à la langue. L’élément peut être spécifié sous la forme d’une plage (par exemple, « 1-12 ») ou d’identificateurs individuels séparés par des espaces blancs (par exemple, « 1 3 4 »).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | Non        | Identificateur de chaîne pour un élément de ressource individuel, à placer dans le fichier de ressources spécifique à la langue. La chaîne peut être spécifiée sous la forme d’une plage (par exemple, « 1-12 ») ou par identificateurs individuels séparés par des espaces blancs (par exemple, « 1 3 4 »). Cet attribut permet de spécifier à la fois les entrées de table de chaînes localisables et celles qui ne sont pas localisables. Elle doit être utilisée conjointement avec la valeur *typeNameId* de « 6 », ce qui dénote un type de ressource d’entrée de table de chaînes.<br/> Les chaînes sont stockées dans des blocs de 16 dans une table de chaînes. Par exemple, les chaînes 0 à 15 sont stockées dans un bloc d’élément de ressource unique et peuvent être référencées dans le fichier de configuration de ressource en tant qu' *ItemId* 1, ou en tant que *stringid* « 0-15 ». Par exemple, s’il existe cinq chaînes localisables et trois chaînes qui ne sont pas localisables, vous devez assigner des identificateurs de chaîne 0-4 pour les chaînes localisables et des identificateurs de chaîne 16-18 pour les chaînes qui ne peuvent pas être localisées. Si vous n’organisez pas les chaînes de cette manière, les blocs de chaînes affectés sont placés à la fois dans le fichier LN et dans le fichier de ressources spécifique à la langue.<br/> |



 

Si vous spécifiez les attributs *ItemName*, *ItemId* et/ou *stringid* pour un type de ressource particulier sous l’élément localizedResource, seuls les éléments ou chaînes spécifiés pour le type de ressource désigné sont placés dans le fichier de ressources spécifique à la langue. Si un élément resourceType est spécifié sans nom d’élément explicite, identificateur d’élément ou identificateur de chaîne, tous les éléments du type de ressource spécifié sont placés dans le fichier de ressources spécifique à une langue. Les éléments ou types non répertoriés dans un élément localizedResource sont placés dans le fichier LN.

Voici les types de ressources standard et leurs identificateurs numériques :

-   CURSOR (1)
-   BITMAP (2)
-   ICÔNE (3)
-   MENU (4)
-   BOÎTE DE DIALOGUE (5)
-   CHAÎNE (6)
-   FONTDIR (7)
-   POLICE (8)
-   ACCÉLÉRATEURS (9)
-   RCDATA (10)
-   MESSAGETABLE (11)
-   \_Curseur de groupe (12)
-   \_Icône de groupe (14)
-   VERSION (16)
-   HTML (23)

## <a name="example"></a>Exemple


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a>Notes

Si vous incluez des types de ressources icône (3), boîte de dialogue (5), chaîne (6) ou VERSION (16) dans l’élément neutralResources, vous devez dupliquer cette entrée dans l’élément localizedResources. Vous pouvez voir ce qui est illustré dans l’exemple ci-dessus, où le type de ressource 16 apparaît dans les sections ressources neutres et ressources localisées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Préparation des ressources](preparing-resources.md)
</dt> </dl>

 

 




