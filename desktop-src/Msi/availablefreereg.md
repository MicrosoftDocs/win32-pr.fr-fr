---
description: La propriété AVAILABLEFREEREG spécifie, en kilo-octets, l’espace libre total disponible dans le registre après l’appel de l’action AllocateRegistrySpace. La valeur maximale de la propriété AVAILABLEFREEREG est de 2 millions kilo-octets. cette propriété est définie uniquement sur Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propriété AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45508494f9ba87ec8261b38ea18f83d0b3ad9796f7390b70349211cbf244df3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650069"
---
# <a name="availablefreereg-property"></a>Propriété AVAILABLEFREEREG

La propriété **AVAILABLEFREEREG** spécifie, en kilo-octets, l’espace libre total disponible dans le registre après l’appel de l' [action AllocateRegistrySpace](allocateregistryspace-action.md).

La valeur maximale de la propriété **AVAILABLEFREEREG** est de 2 millions kilo-octets.

cette propriété est définie uniquement sur Windows 2000.

## <a name="remarks"></a>Remarques

La propriété **AVAILABLEFREEREG** doit être définie sur une valeur suffisamment grande pour garantir un espace suffisant dans le registre pour toutes les informations d’inscription ajoutées par l’installation. La valeur minimale requise pour garantir un espace suffisant dépend de l’emplacement de l' [action AllocateRegistrySpace](allocateregistryspace-action.md) dans la séquence d’action, car le programme d’installation augmente automatiquement l’espace en fonction des besoins lors de l’enregistrement des informations dans les tables [Registry](registry-table.md), [Class](class-table.md), [Selfreg](selfreg-table.md), [extension](extension-table.md), [MIME](mime-table.md)et [verb](verb-table.md) . Le programme d’installation n’augmente pas l’espace total du Registre à la quantité spécifiée par **AVAILABLEFREEREG** jusqu’à atteindre AllocateRegistrySpace dans la séquence d’action.

Si AllocateRegistrySpace est l’une des premières actions de la séquence d’action, **AVAILABLEFREEREG** doit être défini sur l’espace total requis par les informations d’inscription dans la table du Registre, la table de classes, la table Typelib, la table Selfreg, la table d’extension, la table MIME, la table de verbes, l’inscription des [actions personnalisées](custom-actions.md) , l’inscription automatique et toutes les autres informations de Registre écrites La valeur de **AVAILABLEFREEREG** est la quantité totale d’informations ajoutées par l’installation et garantit un espace suffisant dans tous les cas. C’est également le cas le plus courant.

Si l’action AllocateRegistrySpace peut être créée dans la séquence d’action après toutes les [actions standard](standard-actions.md) qui écrivent des données d’inscription, telles que [WriteRegistryValues](writeregistryvalues-action.md) et [RegisterClassInfo](registerclassinfo-action.md), la valeur de **AVAILABLEFREEREG** doit uniquement être définie sur l’espace nécessaire pour enregistrer des actions personnalisées, inscrire des bibliothèques de types et toute autre information non encore inscrite dans les tables.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




