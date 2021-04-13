---
title: Fonctions du gestionnaire de groupe de multidiffusion
description: Les fonctions suivantes sont utilisées pour s’inscrire auprès du gestionnaire de groupe de multidiffusion
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311122"
---
# <a name="multicast-group-manager-functions"></a>Fonctions du gestionnaire de groupe de multidiffusion

Les fonctions suivantes sont utilisées pour s’inscrire auprès du gestionnaire de groupe de multidiffusion :

[**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

Les fonctions suivantes sont utilisées pour gérer la propriété de l’interface :

[**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

Les fonctions suivantes sont utilisées pour gérer l’appartenance à un groupe :

[**MgmAddGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[**MgmDeleteGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

Les fonctions suivantes sont utilisées pour obtenir les entrées de transfert de multidiffusion (MFEs) et les statistiques MFE :

[**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

La fonction suivante est utilisée pour modifier MFEs :

[**MgmSetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

Les fonctions suivantes sont utilisées pour obtenir la liste des groupes qui ont été joints :

[**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




