---
description: Gestion et maintenance des images de déploiement (DISM, Deployment Image Servicing and Management)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestion et maintenance des images de déploiement (DISM, Deployment Image Servicing and Management)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6da1cc8ec3e77a6c63df8e44917cb5f3474ae8e7a5e34b58f49255fa34b5b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053177"
---
# <a name="deployment-image-servicing-and-management-dism"></a>Gestion et maintenance des images de déploiement (DISM, Deployment Image Servicing and Management)

## <a name="affected-platforms"></a>Plateformes affectées

**Clients** -Windows Vista SP1 et versions ultérieures \| Windows 7  
**serveurs** -Windows server 2008 RTM et versions ultérieures \| Windows server 2008 R2  


## <a name="description"></a>Description

l’outil gestion et maintenance des images de déploiement (DISM) remplace les outils pkgmgr, PEImg et IntlConfg en cours de mise hors service dans Windows 7. DISM fournit un outil centralisé unique pour effectuer toutes les fonctions de ces trois outils de manière plus efficace et standardisée, ce qui élimine la source de nombreuses frustrations rencontrées par les utilisateurs actuels de ces outils.

dism comprend un shim pour Windows Vista SP1 et versions ultérieures, ainsi que pour Windows Server 2008 RTM et versions ultérieures, qui redirige les appels pkgmgr à partir d’applications héritées exécutées sur Windows 7 vers DISM. Si l’application s’exécute sur l’un des systèmes d’exploitation pris en charge, le shim achemine l’appel à Pkgmgr. Il n’existe aucun shim pour les applications héritées qui appellent PEImg ou IntlConfg.

## <a name="usage"></a>Usage

DISM est transparent pour les utilisateurs finaux de pkgmgr sur les plateformes prises en charge. toutefois, si une application appelle PEImg ou IntlConfg à partir de Windows 7, l’appel échoue.

Mettez à jour tous les scripts qui appellent pkgmgr, PEImg ou IntlConfg pour appeler DISM à la place. il est important d’inclure la mise à jour des scripts pkgmgr dans le cadre de cet effort, car le shim qui fournit la compatibilité descendante pour pkgmgr sera supprimé dans les versions ultérieures des systèmes d’exploitation Windows.

Vérifiez que les appels à DISM ont remplacé les appels à pkgmgr, PEImg et IntlConfg, et que l’opération s’exécute correctement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion et maintenance des images de déploiement (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))
</dt> </dl>

 

 
