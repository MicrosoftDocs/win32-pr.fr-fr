---
title: Ouverture et fermeture de fichiers
description: Ouverture et fermeture de fichiers
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen fonction)
- AVIFileRelease fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368700"
---
# <a name="opening-and-closing-files"></a>Ouverture et fermeture de fichiers

Une application doit ouvrir un fichier AVI avant la lecture ou l’écriture. Pour ouvrir un fichier AVI, utilisez la fonction [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . **AVIFileOpen** retourne l’adresse d’une interface de fichier AVI qui contient le handle du fichier ouvert et incrémente le décompte de références du fichier.

La fonction **AVIFileOpen** prend en charge le d’indicateurs utilisés avec la fonction [OpenFile](/documentation/) . Si une application écrit dans un fichier existant, elle doit inclure l' \_ indicateur d’écriture dans **AVIFileOpen**. De même, si votre application crée et écrit dans un nouveau fichier, vous devez inclure le de \_ Create et des \_ indicateurs d’écriture dans **AVIFileOpen**.

Lorsque vous ouvrez un fichier à l’aide de **AVIFileOpen**, vous pouvez utiliser un gestionnaire de fichiers par défaut ou vous pouvez spécifier un gestionnaire de fichiers personnalisé pour lire et écrire dans le fichier et ses flux de données. Dans les deux cas, AVIFile recherche le gestionnaire de fichiers correct à utiliser dans le registre. Vous devez vous assurer que les gestionnaires de fichiers personnalisés se trouvent dans le registre avant qu’une application puisse y accéder.

Vous pouvez incrémenter le décompte de références d’un fichier à l’aide de la fonction [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) . Par exemple, vous souhaiterez peut-être effectuer cette opération lors du passage d’un handle de l’interface de fichier à une autre application, ou lorsque vous souhaitez conserver un fichier ouvert lors de l’utilisation d’une fonction qui fermerait normalement le fichier.

Vous pouvez fermer un fichier à l’aide de la fonction [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) . La fonction **AVIFileRelease** décrémente le décompte de références d’un fichier AVI, enregistre les modifications apportées au fichier et, lorsque le nombre de références atteint zéro, ferme le fichier. Vos applications doivent équilibrer le nombre de références en incluant un appel à **AVIFileRelease** pour chaque utilisation de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) et **AVIFileAddRef**.

> [!Note]  
> Une application peut ouvrir un fichier avec un ou plusieurs threads de programme. Toutefois, pour des performances optimales, un seul thread doit accéder au fichier à un moment donné.

 

 

 