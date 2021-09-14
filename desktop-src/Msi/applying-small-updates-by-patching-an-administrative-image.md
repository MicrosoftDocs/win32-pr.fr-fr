---
description: Une installation d’administration crée une image source d’une application ou d’un produit sur un réseau.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Application de petites mises à jour en corrigeant une image administrative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092653"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a>Application de petites mises à jour en corrigeant une image administrative

Une [installation d’administration](administrative-installation.md) crée une image source d’une application ou d’un produit sur un réseau. Les utilisateurs d’un groupe de travail qui ont accès à cette image administrative peuvent installer le produit à partir de cette source. La mise à jour de l’application pour ce groupe de travail s’effectue en deux étapes :

-   Tout d’abord, le correctif de mise à jour de petite taille peut être appliqué à l’image administrative.
-   Deuxièmement, les modifications apportées à la petite mise à jour doivent être propagées aux utilisateurs.

**Pour appliquer un correctif de mise à jour de petite taille à une image administrative**

1.  Obtenez la petite mise à jour sous la forme d’un [package de correctifs](patch-packages.md). Par exemple, la petite mise à jour nommée patch. msp.
2.  Obtenez le chemin d’accès à l’image administrative.
3.  À partir de la ligne de commande, utilisez :

    **msiexec/a** *\[ chemin de l’image administrative .msi \] fichier* **/p** *patch. msp*

4.  Cela met à jour les fichiers d’application et le fichier .msi de l’image administrative. Pour obtenir la liste des options qui peuvent être utilisées avec Msiexec.exe, consultez [options de ligne de commande](command-line-options.md). Windows Le programme d’installation détermine automatiquement si l’image administrative utilise des noms de fichiers courts et définit la propriété [**SHORTFILENAMES**](shortfilenames.md) .
5.  L’image administrative résultante est la même que celle produite par une installation d’administration à l’aide d’un CD-ROM du produit complet qui comprend la mise à jour. Lorsque de nouveaux utilisateurs installent l’application à partir de cette source, ils reçoivent l’application mise à jour.

**Pour propager la petite mise à jour au groupe de travail**

-   Les membres du groupe de travail obtiennent les modifications en réinstallant l’application à partir de l’image administrative à l’aide de la procédure décrite dans [application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md).

 

 



