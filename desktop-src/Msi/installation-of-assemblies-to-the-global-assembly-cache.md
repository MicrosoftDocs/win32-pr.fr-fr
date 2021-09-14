---
description: le Windows Installer installe les assemblys common language runtime dans le Global Assembly Cache à l’aide de la .NET Framework Microsoft.
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: Installation d’assemblys dans le global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121734"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>Installation d’assemblys dans le global assembly cache

le Windows Installer installe les assemblys common language runtime dans le Global Assembly Cache à l’aide de la .NET Framework Microsoft. lors de l’installation d’assemblys dans le Global Assembly Cache, le programme d’installation ne peut pas utiliser la même structure de répertoire et les mêmes règles de version de fichier qu’il utilise lors de l’installation des composants de Windows Installer normaux. les composants de Windows Installer standard peuvent être installés dans plusieurs emplacements de répertoires par différents produits. Les assemblys ne peuvent exister qu’une seule fois dans le cache d’assembly. Chaque assembly est ajouté et supprimé du cache de l’assembly en tant qu’un entier indivisible ; par conséquent, tous les fichiers qui composent un assembly sont toujours installés ou supprimés ensemble.

le coût du disque des composants de Windows Installer normaux et des assemblys de common language runtime est calculé différemment. le coût total de disque d’un composant de Windows Installer régulière comprend les coûts locaux, les coûts de source et les coûts de suppression. Pour plus d’informations, consultez [coûts des fichiers](file-costing.md). cette méthode ne peut pas être utilisée pour le coût common language runtime assemblys, car ceux-ci peuvent avoir des clients autres que le Windows Installer. le coût des assemblys de common language runtime doit être déterminé en interrogeant le common language runtime de .NET Framework Microsoft.

le Windows Installer utilise un processus transactionnel en deux étapes pour installer des produits contenant common language runtime assemblys. Cela permet la restauration de l’installation et de la suppression de l’assembly. Pour plus d’informations, consultez [restauration d’assemblys dans le global assembly cache](rollback-of-assemblies-in-the-global-assembly-cache.md).

notez que les assemblys installés dans le Global Assembly Cache par une installation dans le contexte d' [installation](installation-context.md) par utilisateur ne sont pas protégés par Windows Protection des fichiers. les assemblys installés dans le Global Assembly Cache par une installation dans le contexte d’installation par ordinateur sont protégés par des [Protection des ressources Windows](../wfp/windows-resource-protection-portal.md).

 

 
