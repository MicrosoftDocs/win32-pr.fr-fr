---
title: Installation et suppression du compresseur et du décompresseur
description: Installation et suppression du compresseur et du décompresseur
ms.assetid: 1f00d86f-a777-4bf8-8290-96cc83b2f331
keywords:
- Gestionnaire de compression vidéo (VCM), installation de compresseurs
- VCM (gestionnaire de compression vidéo), installation de compresseurs
- ICInstall fonction)
- ICRemove fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd65f0fc06dc1d5e90cb136f5cf4ea429c220d77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021218"
---
# <a name="compressor-and-decompressor-installation-and-removal"></a>Installation et suppression du compresseur et du décompresseur

une application peut utiliser des compresseurs et des décompresseurs qui sont déjà installés sur un système exécutant le système d’exploitation Microsoft Windows. Une application peut également installer des compresseurs et des décompresseurs pour des utilisations générales ou spéciales. La plupart des applications n’ont pas besoin d’installer ou de supprimer des compresseurs ou des décompresseurs, car ils sont généralement installés par un programme d’installation. Toutefois, une application peut installer un compresseur directement ou installer une fonction en tant que compresseur.

Une application peut installer un compresseur ou un décompresseur (ou une fonction utilisée comme compresseur ou décompresseur) à l’aide de la fonction [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) . Cette fonction crée une entrée dans le registre identifiant le compresseur ou le décompresseur. Votre application ou une autre application peut effectuer des recherches dans le registre pour déterminer si le système contient un compresseur ou un décompresseur adapté à ses données. Utilisez **ICInstall** pour installer tous les pilotes de compression et de décompression.

Une application peut localiser et ouvrir un compresseur ou décompresseur installé à l’aide des fonctions [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) et [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) . Quand une application se termine à l’aide d’un compresseur ou d’un décompresseur, elle la ferme à l’aide de la fonction [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose) .

Une application peut supprimer l’entrée de registre d’un compresseur ou d’un décompresseur installé à l’aide de la fonction [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove) . Cette fonction supprime l’entrée de registre d’un compresseur ou d’un décompresseur qui n’est pas actuellement chargé dans la mémoire.

Une application peut restreindre l’utilisation d’un compresseur ou d’un décompresseur en l’installant, en l’ouvrant, en la fermant et en le supprimant.

En guise d’alternative, pour utiliser une fonction en interne en tant que compresseur ou décompresseur sans l’installer dans le registre, une application peut utiliser la fonction [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction) . Pour cette fonction, l’application appelante doit avoir l’adresse de la fonction à utiliser comme compresseur ou décompresseur. Lorsque l’application se termine à l’aide de la fonction, elle doit la fermer à l’aide de **ICClose**. Étant donné que la fonction n’a pas été installée, l’application n’a pas besoin de supprimer la fonction du Registre.

La structure interne d’une fonction utilisée comme compresseur ou décompresseur doit être la même que la fonction de point d’entrée [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) utilisée par les pilotes installables. Pour plus d’informations sur la fonction de point d’entrée **DriverProc** , consultez [pilotes installables](installable-drivers.md).

> [!Note]  
> Une application qui installe une fonction en tant que compresseur ou décompresseur doit supprimer la fonction avant la fermeture de l’application afin que d’autres applications n’essaient pas d’utiliser la fonction. Lors de la suppression d’une fonction, l’application doit l’identifier avec le code à quatre caractères utilisé pour l’installer.

 

 

 