---
title: Suivi des plages modifiées d’un fichier
description: Suivi des plages modifiées d’un fichier
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106509883"
---
# <a name="tracking-modified-ranges-of-a-file"></a>Suivi des plages modifiées d’un fichier

## <a name="platforms"></a>Plateformes

**Clients-** Windows 8.1 (toutes les références SKU)  
**Serveurs-** Windows Server 2012 R2  

## <a name="description"></a>Description

L’équipe du système de fichiers NT (NTFS) a ajouté une nouvelle fonctionnalité à Windows. Le journal USN génère un enregistrement de numéro de séquence de mise à jour (USN) contenant des plages modifiées pour un fichier lors de la fermeture. Un nouveau type d’enregistrement, l' \_ enregistrement USN \_ v4 a été introduit pour enregistrer ces plages modifiées d’un fichier.

La fonctionnalité n’est pas activée par défaut ; les utilisateurs doivent appeler une commande de contrôle de système de fichiers (FSCTL) pour l’activer. Toutefois, étant donné que d’autres composants Windows peuvent activer le suivi des plages, les utilisateurs et les développeurs peuvent percevoir que la fonctionnalité est toujours activée. Windows permettra aux développeurs d’interroger le journal USN pour déterminer si le suivi des plages est activé.

La documentation MSDN sera fournie à une date ultérieure pour indiquer aux développeurs comment accéder aux \_ enregistrements v4 de l’enregistrement USN \_ .

## <a name="manifestation"></a>Manifestation

Toutes les applications existantes qui utilisent le journal USN continuent de fonctionner correctement, sans aucun problème de compatibilité.

 

 




