---
description: Windows utilise un pointeur de fichier pour effectuer le suivi des octets lus ou écrits.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Positionnement d’un pointeur de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93caefcb622f297d391aba4d695a2b0c2c2e2ca368a97c68332862a7f8bfa8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951088"
---
# <a name="positioning-a-file-pointer"></a>Positionnement d’un pointeur de fichier

quand une application appelle [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pour ouvrir un fichier pour la première fois, Windows place le [pointeur de fichier](file-pointers.md) au début du fichier. au fur et à mesure que les octets sont lus ou écrits dans le fichier, Windows avance le pointeur de fichier le nombre d’octets lus ou écrits.

Une application peut positionner le pointeur de fichier sur un offset spécifié en appelant [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).

La fonction [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) peut également être utilisée pour interroger la position actuelle du pointeur de fichier en spécifiant une méthode Move du **fichier \_ Current** et une distance de zéro.

 

 



