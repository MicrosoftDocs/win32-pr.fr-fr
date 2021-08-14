---
title: sauvegarde et restauration de Windows 7 déconseillées
description: sauvegarde et restauration de Windows 7 déconseillées
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211228"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>sauvegarde et restauration de Windows 7 déconseillées

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


## <a name="description"></a>Description

Bien qu’il n’y ait pas de modification comportementale de la sauvegarde et de la restauration, cette fonction est déconseillée et ne sera pas mise à jour. Il était rarement utilisé et ses fonctionnalités ont été remplacées par la nouvelle fonctionnalité historique des fichiers. elle est fournie en Windows 8 et passionnés qui ont été mis à niveau de Windows 7 à Windows 8 ou qui dépendent de la sauvegarde et de la restauration ou de la sauvegarde d’image disque sera toujours en mesure de l’utiliser. Toutefois, tous les points d’accès à la sauvegarde et à la restauration, à l’exception du panneau de configuration, ont été supprimés. l’applet du panneau de configuration utilisée par la sauvegarde et la restauration a été renommée en Windows 7 fichiers récupérés.

Les OEM qui configurent la clé de Registre pour désactiver la notification de sauvegarde dans leurs images n’ont plus besoin de le faire.

Nous vous déconseillons d’utiliser les deux fonctionnalités en même temps. L’historique des fichiers vérifie si la planification de sauvegarde existe et est active et si elle en trouve une, elle ne permet pas aux utilisateurs de l’activer. dans ce cas, les utilisateurs qui souhaitent utiliser l’historique des fichiers devront supprimer la planification de Sauvegarde Windows.

## <a name="manifestation"></a>Manifestation

les flux de travail peuvent être interrompus et la documentation qui fait référence à la méthode précédente pour accéder au Sauvegarde Windows et restaurer la fonctionnalité doit être mise à jour pour refléter ces modifications.

## <a name="mitigation"></a>Limitation des risques

Les applications qui peuvent déclencher la sauvegarde et la restauration doivent être réécrites pour vérifier si l’historique des fichiers est activé et permettre aux utilisateurs de choisir leur méthode préférée.

 

 




