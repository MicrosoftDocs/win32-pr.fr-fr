---
description: La définition de la valeur de cette stratégie système par ordinateur sur &\# 0034 ; 1&\# 0034 ; permet aux utilisateurs non administratifs d’utiliser une boîte de dialogue Parcourir pour localiser les sources des applications gérées.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864498"
---
# <a name="allowlockdownbrowse"></a>AllowLockdownBrowse

La définition de la valeur de cette [stratégie système](system-policy.md) par ordinateur sur « 1 » permet aux utilisateurs non administratifs d’utiliser une [boîte de dialogue Parcourir](browse-dialog.md) pour localiser les sources des [*applications gérées*](m-gly.md). Les sources peuvent inclure des médias, tels que des CD-ROM, des URL et des emplacements réseau. Pour plus d’informations, consultez [résilience source](source-resiliency.md). La valeur par défaut sur Windows Installer est que les utilisateurs non administratifs ne peuvent pas rechercher de nouvelles sources d’applications gérées. Les seules sources disponibles sont celles qui sont déjà inscrites dans la liste source du produit. Si cette stratégie est définie, un utilisateur non administratif peut rechercher de nouvelles sources d’applications ou d’applications attribuées ou publiées en cours d’installation pour tous les utilisateurs. La définition de AllowLockdownBrowse permet également aux utilisateurs non administratifs d’exécuter des programmes sur des privilèges LocalSystem au cours d’une installation avec élévation de privilèges.

Le paramètre par défaut est recommandé pour garantir un environnement sécurisé.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="remarks"></a>Notes

La définition de cette stratégie permet également aux utilisateurs non administratifs d’exécuter des programmes arbitraires sur des privilèges LocalSystem s’ils disposent d’un package Windows Installer qui installe ou lance ces programmes.

[DisableBrowse](disablebrowse.md) remplace AllowLockdownBrowse et empêche la navigation même si AllowLockdownBrowse est défini.

Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résilience source](source-resiliency.md)
</dt> <dt>

[AllowLockdownMedia](allowlockdownmedia.md)
</dt> </dl>

 

 



