---
title: Lire à partir d’un fichier
description: Lire à partir d’un fichier
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95186b1ec8913623b0ab02e0d2bc5556302d4dcd03f7737ac12c5872b9f2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371684"
---
# <a name="reading-from-a-file"></a>Lire à partir d’un fichier

Vous pouvez récupérer des informations sur un fichier ouvert à l’aide de la fonction [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) . Cette fonction remplit la structure [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) avec des informations telles que le débit de données maximal, le nombre de flux dans le fichier, si le fichier utilise un index et si le fichier est protégé par des droits d’auteur.

Pour récupérer des informations supplémentaires dans un fichier AVI, utilisez la fonction [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) . Des informations supplémentaires sont applicables à l’ensemble du fichier et ne sont pas incluses dans les en-têtes de fichier normaux. Par exemple, le nom de la société ou de la personne qui détient les droits d’auteur d’un fichier peut être des informations supplémentaires. Les informations supplémentaires ne sont pas conformes à un format spécifique. Il peut s’agir d’un fichier spécifique. **AVIFileReadData** retourne les informations supplémentaires dans une mémoire tampon fournie par l’application.

 

 




