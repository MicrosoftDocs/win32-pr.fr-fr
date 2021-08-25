---
description: 'Les fonctions suivantes permettent à une application d’enregistrer, de restaurer et de réinitialiser un contexte de périphérique : SaveDC, RestoreDC et ResetDC.'
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Enregistrement, restauration et réinitialisation d’un contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 434ef484fecee17251a31616e396ee0fa66b381bc30cf858575f4455ca36a1ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965249"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Enregistrement, restauration et réinitialisation d’un contexte de périphérique

Les fonctions suivantes permettent à une application d’enregistrer, de restaurer et de réinitialiser un contexte de périphérique : [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)et [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). La fonction SaveDC enregistre sur une pile GDI spéciale les objets graphiques du DC actuel et leurs attributs, ainsi que les modes graphiques. Une application de dessin peut appeler cette fonction avant que l’utilisateur commence à dessiner et à enregistrer l’état d’origine de l’application, ce qui fournit une ardoise propre à l’utilisateur. Pour revenir à cet état d’origine, l’application appelle la fonction RestoreDC.

[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) est fourni pour réinitialiser les données DC de l’imprimante. Une application appelle cette fonction pour réinitialiser l’orientation du papier, le format de papier, le facteur d’échelle de sortie, le nombre de copies à imprimer, la source de papier (ou l’emplacement), le mode duplex, etc. En règle générale, une application appelle cette fonction après qu’un utilisateur a modifié l’une des options d’imprimante et que le système a émis un message [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) .

 

 



