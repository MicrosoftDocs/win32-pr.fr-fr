---
title: Icônes de classe
description: L’icône utilisée pour représenter un objet de classe peut être spécifiée dans l’attribut iconPath du conteneur DisplaySpecifiers.
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- noms d’affichage de classes Active Directory, icônes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022600"
---
# <a name="class-icons"></a>Icônes de classe

L’icône utilisée pour représenter un objet de classe peut être spécifiée dans l’attribut **iconPath** du conteneur DisplaySpecifiers. En outre, chaque classe peut stocker plusieurs États d’icône. Par exemple, une classe de dossiers peut avoir des icônes pour les États Open, Closed et Disabled. L’implémentation actuelle accepte un maximum de seize États d’icône différents par classe.

L’attribut **iconPath** peut être spécifié de deux façons.


```C++
<state>,<icon file name>
```



ou


```C++
<state>,<module file name>,<resource ID>
```



Dans ces exemples, « &lt; State &gt; » est un entier dont la valeur est comprise entre 0 et 15. La valeur 0 est définie comme étant l’État par défaut ou fermé de l’icône. La valeur 1 est définie pour être l’état ouvert de l’icône. La valeur 2 est l’état désactivé. Toutes les autres valeurs sont définies par l’application.

« &lt; Icon File name &gt; » est le chemin d’accès et le nom de fichier d’un fichier d’icône qui contient l’image d’icône.

Le « &lt; nom de fichier du module &gt; » est le chemin d’accès et le nom de fichier d’un module, tel qu’un exe ou une dll, qui contient l’image d’icône dans une ressource. L' &lt; ID de ressource &gt; est un entier qui spécifie l’identificateur de ressource de la ressource icône dans le module.

## <a name="adding-a-value-to-the-iconpath-attribute"></a>Ajout d’une valeur à l’attribut **iconPath**

Pour ajouter une valeur à l’attribut **iconPath** , procédez comme suit.

1.  Déterminez si la valeur de l’attribut existe. Si une valeur doit être remplacée, supprimez d’abord la valeur existante à l’aide de la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **ADS \_ propriété \_ Delete** et le paramètre *vProp* défini sur la valeur à supprimer. N’utilisez pas **les \_ Propriétés ad \_ Clear** ou **ADS \_ Property \_ Update** pour *lnControlCode*.
2.  Créez la chaîne qui représente les données de l’icône d’attribut. Pour obtenir un exemple, consultez le format ci-dessus.
3.  Pour ajouter la nouvelle valeur, utilisez la méthode [**IADs ::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) avec le paramètre *LnControlCode* défini sur **ADS \_ propriété \_ Append**.
4.  Pour valider les modifications apportées à l’annuaire, appelez [**IADs :: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 