---
title: Partage d’une procédure d’e/s avec d’autres applications
description: Partage d’une procédure d’e/s avec d’autres applications
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de fichier multimédia, procédures partagées
- e/s de fichier, procédures partagées
- entrées et sorties (e/s), procédures partagées
- E/s (entrée et sortie), procédures partagées
- partage de procédures d’e/s avec d’autres applications
- mmioInstallIOProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368447"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Partage d’une procédure d’e/s avec d’autres applications

Si vous souhaitez partager une procédure d’e/s avec d’autres applications, vous devez écrire une bibliothèque de liens dynamiques (DLL) pour votre application. Vous pouvez partager la procédure d’e/s en procédant de l’une des manières suivantes :

-   Incluez le code de la procédure d’e/s dans la DLL.
-   Créez une fonction dans la DLL qui appelle la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) pour installer la procédure d’e/s.
-   Exportez cette fonction dans le fichier de définitions de module de la DLL.

Pour utiliser la procédure d’e/s partagée, une application doit d’abord appeler la fonction dans la DLL pour installer la procédure d’e/s.

 

 