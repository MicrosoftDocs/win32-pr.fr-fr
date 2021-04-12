---
description: Une version de qualificateur est un indicateur qui décrit des informations supplémentaires sur un qualificateur.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Description d’un qualificateur avec une version de qualificateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202293"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>Description d’un qualificateur avec une version de qualificateur

Une [*version de qualificateur*](gloss-q.md) est un indicateur qui décrit des informations supplémentaires sur un qualificateur. Par exemple, la version de qualificateur restreint indique que WMI ne doit pas propager le qualificateur associé à une instance ou à une classe dérivée. Vous pouvez définir des versions à l’aide d’un code MOF ou par programme. Bien que vous puissiez décrire divers effets avec des versions, les principaux objectifs des indicateurs Flavors sont de définir comment WMI propage les qualificateurs par héritage.

WMI définit plusieurs versions de qualificateur que vous pouvez attacher à n’importe quel qualificateur, quelle que soit l’origine du qualificateur. Toutefois, certaines versions ne sont pas appropriées pour tous les types de qualificateurs. Par exemple, la version **ToSubClass** est appropriée uniquement pour les qualificateurs définis pour une classe. Vous ne pouvez pas joindre **ToSubClass** à un qualificateur utilisé pour décrire une instance.

Vous pouvez utiliser des versions pour décrire divers effets différents pour les qualificateurs. Par exemple, la version peut indiquer si un qualificateur peut être localisé. Toutefois, l’un des principaux objectifs d’une version de qualificateur est de décrire si une classe parente peut passer des qualificateurs à une sous-classe ou à une instance de classe. Vous pouvez également utiliser des versions pour déterminer si une propriété de classe passe un qualificateur à une propriété d’instance. Enfin, utilisez des versions pour indiquer si une sous-classe peut remplacer la valeur d’origine d’un qualificateur hérité. Toutefois, les qualificateurs que vous déclarez pour une classe ou une instance ne se propagent pas aux propriétés de cette classe ou instance. En outre, les versions qui établissent des autorisations de remplacement ne sont valides que si vous définissez également les versions **ToInstance** ou **ToSubClass** .

Une version peut être affectée globalement à un qualificateur pour l’intégralité d’un fichier MOF à l’aide de la syntaxe suivante, dans laquelle l’espace blanc agit comme séparateur lorsque plusieurs versions sont spécifiées.

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

Les versions globales s’appliquent à toutes les utilisations suivantes du qualificateur dans le fichier MOF. Les instructions de version globale peuvent se trouver n’importe où dans le fichier en dehors d’un bloc de déclaration d’objet. Les parfums redéfinis au niveau de la classe, de l’instance ou de la propriété remplacent les déclarations de arôme global pour la portée de cet objet.

Vous ne pouvez pas définir une nouvelle version. Bien que vous puissiez créer un qualificateur, utilisez uniquement des [versions de qualificateur](qualifier-flavors.md) existantes pour décrire votre nouveau qualificateur.

**Pour définir des versions de qualificateur dans MOF**

-   Déclarez les versions qui décrivent un qualificateur donné après le nom du qualificateur, entre les crochets du qualificateur. Utilisez un espace blanc comme délimiteur entre plusieurs versions.

    L’exemple suivant illustre le modèle d’attachement de qualificateurs prédéfinis.

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

Vous pouvez ajouter des versions de qualificateur par programmation uniquement en C++. Cette opération n’est pas disponible dans l' [API de script pour WMI](scripting-api-for-wmi.md), bien que vous puissiez ajouter un nouveau qualificateur en appelant [**SWbemQualifierSet. Add**](swbemqualifierset-add.md).

**Pour assigner une version à l’aide de C++**

-   Appelez la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) avec le paramètre *lFlavor* défini sur l’une des constantes définies pour la méthode.

 

 



