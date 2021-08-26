---
description: Le&XPS \# 160 ; Imprimer&\# 160 ; L’API fournit une interface au spouleur d’impression que les applications peuvent utiliser pour imprimer des travaux qui envoient des documents XPS à une imprimante.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: À propos de l’API d’impression XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950859"
---
# <a name="about-the-xps-print-api"></a>À propos de l’API d’impression XPS

L' [API d’impression XPS](xps-printing.md) fournit une interface au spouleur d’impression que les applications peuvent utiliser pour imprimer des travaux qui envoient des documents XPS à une imprimante.

Si l’imprimante de destination utilise un pilote d’imprimante XPSDrv, l’API d’impression XPS permet au pilote d’imprimante XPSDrv de recevoir des événements de document lorsque le spouleur d’impression traite un travail d’impression. Pour obtenir une description des événements de document envoyés au pilote d’imprimante XPSDrv, consultez [événements de document du pilote XPS](/windows-hardware/drivers/print/xps-driver-document-events).

Si l’imprimante de destination utilise un pilote d’imprimante GDI, l' [API d’impression XPS](xps-printing.md) permet au système de gérer la conversion nécessaire des données du travail d’impression à partir du format XPS au format EMF (métafichier amélioré) utilisé par le pilote d’imprimante GDI. Pour obtenir une description des événements de document du pilote d’imprimante GDI, consultez [fonction DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’API d’impression XPS](using-the-xps-print-api.md)
</dt> <dt>

[Informations de référence sur l’API d’impression XPS](xpsprint-api.md)
</dt> </dl>

 

 
