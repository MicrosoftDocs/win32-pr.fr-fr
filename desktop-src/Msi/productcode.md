---
description: La propriété ProductCode est un identificateur unique pour la version particulière du produit, représenté sous la forme d’un GUID de chaîne, par exemple &\# 0034 ; {12345678-1234-1234-1234-123456789012}&\# 0034 ;.
ms.assetid: 33cedd37-0343-471c-ad4b-0db5f98d5894
title: Propriété ProductCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a77ba270075b214d5eee2ee804c6849a2ef71561610ee60ae3eb4941e43465c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753909"
---
# <a name="productcode-property"></a>Propriété ProductCode

La propriété **ProductCode** est un identificateur unique pour la version particulière du produit, représenté sous la forme d’un [GUID](guid.md)de chaîne, par exemple « {12345678-1234-1234-1234-123456789012} ». Les lettres utilisées dans ce GUID doivent être en majuscules. Cet ID doit varier en fonction des versions et des langues.

Une mise à niveau de produit qui met à jour un produit dans un produit entièrement nouveau doit également modifier le code du produit. Les versions 32 bits et 64 bits du package d’une application doivent se voir assigner des codes de produit différents.

Le **ProductCode** est publié en tant que propriété de produit et constitue la principale méthode de spécification du produit. Cette propriété est obligatoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




