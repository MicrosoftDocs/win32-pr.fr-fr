---
title: Sauvegarde et restauration de Windows 7 déconseillées
description: Sauvegarde et restauration de Windows 7 déconseillées
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106513746"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Sauvegarde et restauration de Windows 7 déconseillées

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Bien qu’il n’y ait pas de modification comportementale de la sauvegarde et de la restauration, cette fonction est déconseillée et ne sera pas mise à jour. Il était rarement utilisé et ses fonctionnalités ont été remplacées par la nouvelle fonctionnalité historique des fichiers. Elle sera commercialisée dans Windows 8 et passionnés de mise à niveau de Windows 7 vers Windows 8, ou qui dépend de la sauvegarde et de la restauration ou de la sauvegarde d’image disque, sera toujours en mesure de l’utiliser. Toutefois, tous les points d’accès à la sauvegarde et à la restauration, à l’exception du panneau de configuration, ont été supprimés. L’applet du panneau de configuration utilisée par la sauvegarde et la restauration a été renommée en récupération de fichiers Windows 7.

Les OEM qui configurent la clé de Registre pour désactiver la notification de sauvegarde dans leurs images n’ont plus besoin de le faire.

Nous vous déconseillons d’utiliser les deux fonctionnalités en même temps. L’historique des fichiers vérifie si la planification de sauvegarde existe et est active et si elle en trouve une, elle ne permet pas aux utilisateurs de l’activer. Dans ce cas, les utilisateurs qui souhaitent utiliser l’historique des fichiers devront supprimer la planification de sauvegarde Windows.

## <a name="manifestation"></a>Manifestation

Les workflows peuvent être interrompus et la documentation qui fait référence à la méthode précédente pour accéder à la fonctionnalité de sauvegarde et de restauration Windows doit être mise à jour pour refléter ces modifications.

## <a name="mitigation"></a>Limitation des risques

Les applications qui peuvent déclencher la sauvegarde et la restauration doivent être réécrites pour vérifier si l’historique des fichiers est activé et permettre aux utilisateurs de choisir leur méthode préférée.

 

 




