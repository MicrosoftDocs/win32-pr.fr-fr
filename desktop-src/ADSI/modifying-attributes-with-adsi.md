---
title: Modification d’attributs avec ADSI
description: Pour modifier des valeurs d’attribut, ADSI fournit les méthodes IADs. put et IADs. biais. Ces méthodes modifient les données dans le cache côté client. La méthode IADs. SetInfo doit être appelée pour valider les modifications apportées au répertoire.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modification d’attributs avec ADSI
- Attributs ADSI, modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079959"
---
# <a name="modifying-attributes-with-adsi"></a>Modification d’attributs avec ADSI

Pour modifier des valeurs d’attribut, ADSI fournit les méthodes [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) biais. Ces méthodes modifient les données dans le cache côté client. La méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) doit être appelée pour valider les modifications apportées au répertoire.

> [!Note]  
> Lorsque plusieurs modifications d’attribut sont validées dans un seul appel à [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), si un attribut unique ne peut pas être modifié, aucun des attributs ne sera modifié. Par exemple, si vous modifiez les attributs [**sn**](/windows/desktop/ADSchema/a-sn) et [**GivenName**](/windows/desktop/ADSchema/a-givenname) et que vous effacez l’attribut [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) d’un objet User sans les appels suivants à la méthode **setinfo** , les modifications sont entrées lorsque vous appelez **setinfo**. Si une ou plusieurs modifications ne sont pas autorisées et ne peuvent donc pas être effectuées, aucune des modifications collectives apportées aux attributs n’est entrée lors de l’appel à **setinfo**.

 

La méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) prend un nom d’attribut et un paramètre Variant. Utilisez cette méthode pour définir des attributs qui contiennent à la fois des valeurs uniques et multiples.

La méthode [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) 2D fournit un contrôle sur les opérations sur les attributs à valeurs multiples. Vous pouvez ajouter, supprimer, mettre à jour et effacer les valeurs existantes. La méthode **IADs .Ed** attend toujours un tableau variant de valeurs d’attribut. Toutefois, vous pouvez utiliser cette méthode pour définir un attribut avec une seule valeur.

La méthode [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) ciblage utilise les opérations spécifiées par l’énumération enum de l' [**opération de \_ propriété \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

 

 