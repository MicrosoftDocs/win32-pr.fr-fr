---
description: L’API du fournisseur réseau spécifie une fonction de fonctions unique.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Fonctions fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034266"
---
# <a name="capabilities-functions"></a>Fonctions fonctions

L’API du fournisseur réseau spécifie une fonction de fonctions unique. Lorsque le système d’exploitation demande des informations sur les fonctionnalités d’un fournisseur de réseau, le [*routeur de fournisseur multiple*](/windows/desktop/SecGloss/m-gly) (MPR) appelle la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de chaque fournisseur réseau dont le réseau est actif.

La fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) renvoie un masque de masque indiquant les fonctions de l’API du fournisseur réseau prises en charge par le fournisseur réseau. La fonction **NPGetCaps** est la seule fonction qu’un fournisseur réseau doit implémenter. Le système d’exploitation appelle cette fonction pour déterminer les autres fonctions de l’API du fournisseur réseau prises en charge par le fournisseur.

 

 
