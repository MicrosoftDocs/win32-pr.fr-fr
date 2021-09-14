---
description: L’action MsiConfigureServices configure un service pour le système. Cette action interroge les tables MsiServiceConfig et MsiServiceConfigFailureActions.
ms.assetid: 63bd4690-0649-4e23-a8cd-527b3c517dae
title: Action MsiConfigureServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f2321bcdfaeede8e80d7f4c341f5a099690952
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011882"
---
# <a name="msiconfigureservices-action"></a>Action MsiConfigureServices

L’action MsiConfigureServices configure un service pour le système. Cette action interroge les tables [MsiServiceConfig](msiserviceconfig-table.md) et [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) .

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. cette action est disponible à partir de Windows Installer 5,0.

> [!IMPORTANT]
>
> Windows Les services permettent d’effectuer automatiquement des actions prédéfinies en réponse à une défaillance dans un service. Pour prendre en charge la configuration par programmation de ces **actions de récupération** en cas d’échec d’un service, [MsiServiceConfigFailureActions](msiserviceconfigfailureactions-table.md) a été ajouté à MSI dans la version MSI 5,0. Toutefois, cette fonctionnalité ne fonctionne pas comme prévu.
>
> Pour contourner ce problème, un développeur d’applications doit utiliser la fonctionnalité d' **action personnalisée** dans MSI pour exécuter **sc.exe** et définir les **options de récupération** de manière appropriée.

 

## <a name="sequence-restrictions"></a>Restrictions de séquence

Cette action standard doit être utilisée dans l’ordre suivant.

[StopServices](stopservices-action.md)

[DeleteServices](deleteservices-action.md)

L’une des actions suivantes : les actions [InstallFiles](installfiles-action.md), [RemoveFiles](removefiles-action.md), [DuplicateFiles](duplicatefiles-action.md), [MoveFiles](movefiles-action.md), [PatchFiles](patchfiles-action.md)et [RemoveDuplicateFiles](removeduplicatefiles-action.md) .

[InstallServices](installservices-action.md)

MsiConfigureServices

[StartServices](startservices-action.md)

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

Cette action nécessite que l’utilisateur soit un administrateur ou qu’il dispose de privilèges élevés avec l’autorisation d’installer des services ou que l’application fasse partie d’une installation gérée.

 

 



