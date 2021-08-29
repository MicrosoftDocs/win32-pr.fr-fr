---
title: Partage des listes d’affichage
description: Lorsque vous créez un contexte de rendu, il possède son propre espace de liste d’affichage.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL sur Windows, partage des listes d’affichage
- partage des listes d’affichage OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934789f3de00e6e0be451fc441416dfcbaa057b0b58b224fc57021db31575e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776629"
---
# <a name="sharing-display-lists"></a>Partage des listes d’affichage

Lorsque vous créez un contexte de rendu, il possède son propre espace de liste d’affichage. La fonction [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permet à un contexte de rendu de partager l’espace de liste d’affichage d’un autre contexte de rendu. Un nombre quelconque de contextes de rendu peut partager un seul espace de liste d’affichage.

 

 




