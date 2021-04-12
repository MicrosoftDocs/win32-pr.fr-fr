---
title: Attributs liés (AD DS)
description: Les attributs liés sont des paires d’attributs dans lesquelles le système calcule les valeurs d’un attribut (lien précédent) en fonction des valeurs définies sur l’autre attribut (le lien suivant) dans toute la forêt.
ms.assetid: 31b7e8f5-e46d-4aff-9b17-c8dec7f19bae
ms.tgt_platform: multiple
keywords:
- Attributs liés AD
- Attributs AD, liés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0e3f6706c797497fb1bb25ea82805385f9897e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104381762"
---
# <a name="linked-attributes-ad-ds"></a>Attributs liés (AD DS)

Les attributs liés sont des paires d’attributs dans lesquelles le système calcule les valeurs d’un attribut (lien précédent) en fonction des valeurs définies sur l’autre attribut (le lien suivant) dans toute la forêt. Une valeur de lien back sur une instance d’objet se compose du DNs de tous les objets dont le DN de l’objet est défini dans le lien suivant. Par exemple, « Manager » et « Reports » sont une paire d’attributs liés, où Manager est le lien suivant et Reports est le lien back. Supposons maintenant que Bill est le responsable de Joe. Si vous stockez le DN de l’objet utilisateur de la facture dans l’attribut « Manager » de l’objet utilisateur de Joe, le DN de l’objet utilisateur de Joe s’affichera dans l’attribut « Reports » de l’objet utilisateur de la facture.

Une paire lien-arrière/lien suivant est identifiée par les valeurs [**LinkId**](/windows/desktop/ADSchema/a-linkid) de deux définitions [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Le **LinkId** du lien suivant est une valeur paire, positive et différente de zéro, et le **LinkId** du lien précédent est le **LinkId** de transfert plus un. Par exemple, le **LinkId** pour « Manager » est 42 et le **LinkId** pour « Reports » est 43.

La liste suivante répertorie les instructions permettant de définir une nouvelle paire d’attributs liés :

-   Les valeurs [**LinkId**](/windows/desktop/ADSchema/a-linkid) doivent être uniques parmi tous les objets [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Pour éviter les conflits, vous devez générer automatiquement le **LinkId** en suivant les instructions de la rubrique [obtention d’un ID de lien](obtaining-a-link-id.md).
-   Un lien précédent doit avoir un lien suivant, autrement dit, le lien suivant doit exister avant qu’un attribut de lien précédent puisse être créé.
-   Un lien précédent est toujours un attribut à valeurs multiples. Un lien suivant peut être à valeur unique ou à valeurs multiples. Utilisez un lien de transfert à valeurs multiples lorsqu’il existe une relation plusieurs-à-plusieurs.
-   La valeur [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) d’un lien suivant doit être 2.5.5.1, 2.5.5.7 ou 2.5.5.14. Ces valeurs correspondent à des syntaxes qui contiennent un nom unique, tel que la syntaxe [**Object (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   La valeur [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) d’un lien précédent doit être 2.5.5.1, qui est la syntaxe de l' [**objet (DS-DN)**](/windows/desktop/ADSchema/s-object-ds-dn) .
-   Par Convention, les attributs de lien Back sont ajoutés à la valeur [**mayContain**](/windows/desktop/ADSchema/a-maycontain) de la classe abstraite [**Top**](/windows/desktop/ADSchema/c-top) . Cela permet de lire l’attribut de lien précédent à partir des objets de toute classe, car ils ne sont pas réellement stockés avec l’objet, mais ils sont calculés en fonction des valeurs de lien de transfert.

 

 