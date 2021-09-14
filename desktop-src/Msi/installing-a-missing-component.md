---
description: vous pouvez utiliser la Windows Installer pour détecter les composants ou fichiers manquants, puis réinstaller les fonctionnalités qui contiennent les composants manquants.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Installation d’un composant manquant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012058"
---
# <a name="installing-a-missing-component"></a>Installation d’un composant manquant

vous pouvez utiliser la Windows Installer pour détecter les composants ou fichiers manquants, puis réinstaller les fonctionnalités qui contiennent les composants manquants. Étant donné que le programme d’installation installe les fonctionnalités et non les composants, il doit d’abord résoudre le composant auquel appartient un fichier manquant, puis installer la fonctionnalité qui contient le composant. Si plusieurs fonctionnalités sont liées au composant, le programme d’installation installe la fonctionnalité qui nécessite le moins d’espace disque.

Si vous appelez [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), vous pouvez vérifier que le fichier de clé d’un composant est présent. Toutefois, il est toujours possible que d’autres fichiers appartenant au composant soient absents. Dans ce scénario, appelez [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). Le programme d’installation se résout ensuite sur le composant auquel le fichier appartient et installe la fonctionnalité liée au composant qui requiert le moins d’espace disque.

Si la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) échoue de façon inattendue, vous devez installer tous les composants manquants.

La procédure suivante montre comment installer les composants manquants.

**Pour détecter et installer un composant manquant**

1.  Appelez [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) pour vérifier que le fichier de clé d’un composant est présent. Toutefois, même si le fichier de clé du composant est présent, il est encore possible que d’autres fichiers appartenant au composant soient manquants.
2.  Appelez la fonction [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) si la fonctionnalité associée au composant est inconnue.
3.  Appelez la fonction [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) ou [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) si la fonctionnalité associée au composant est connue.
4.  Appelez [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) si une application ne parvient pas à ouvrir un fichier.

 

 



