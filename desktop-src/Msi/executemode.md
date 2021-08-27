---
description: La propriété EXECUTEMODE spécifie la façon dont le programme d’installation exécute les mises à jour système.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propriété EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 750b6c3a20ab05388fcd6926463dde8259440bd6087306b1bf0cc1a6c387cd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082869"
---
# <a name="executemode-property"></a>Propriété EXECUTEMODE

La propriété **EXECUTEMODE** spécifie la façon dont le programme d’installation exécute les mises à jour système. Cette propriété peut être utile lorsqu’il est nécessaire d’exécuter une installation sans modifier réellement le système. La propriété peut avoir la valeur None pour désactiver les opérations de mise à jour telles que l’installation de fichiers et de valeurs de registre.

Cette propriété peut avoir l’une des deux valeurs suivantes. Le programme d’installation examine uniquement la première lettre de la valeur et ne respecte pas la casse.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>None
</dt> <dd>

Aucune modification n’est apportée au système. Le programme d’installation exécute l’interface utilisateur, puis interroge la base de données.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Conseils
</dt> <dd>

Toutes les modifications apportées au système sont effectuées par le biais de l’exécution du script. Il s’agit du mode par défaut ;

</dd> </dl>

## <a name="default-value"></a>Valeur par défaut

Si cette propriété n’est pas définie, le mode d’exécution prend par défaut le script.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




