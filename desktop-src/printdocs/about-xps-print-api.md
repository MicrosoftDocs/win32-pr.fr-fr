---
description: Le&XPS \# 160 ; Imprimer&\# 160 ; L’API fournit une interface au spouleur d’impression que les applications peuvent utiliser pour imprimer des travaux qui envoient des documents XPS à une imprimante.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: À propos de l’API d’impression XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115487"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="d9d2d-103">À propos de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d9d2d-103">About the XPS Print API</span></span>

<span data-ttu-id="d9d2d-104">L' [API d’impression XPS](xps-printing.md) fournit une interface au spouleur d’impression que les applications peuvent utiliser pour imprimer des travaux qui envoient des documents XPS à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="d9d2d-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="d9d2d-105">Si l’imprimante de destination utilise un pilote d’imprimante XPSDrv, l’API d’impression XPS permet au pilote d’imprimante XPSDrv de recevoir des événements de document lorsque le spouleur d’impression traite un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d9d2d-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="d9d2d-106">Pour obtenir une description des événements de document envoyés au pilote d’imprimante XPSDrv, consultez [événements de document du pilote XPS](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="d9d2d-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="d9d2d-107">Si l’imprimante de destination utilise un pilote d’imprimante GDI, l' [API d’impression XPS](xps-printing.md) permet au système de gérer la conversion nécessaire des données du travail d’impression à partir du format XPS au format EMF (métafichier amélioré) utilisé par le pilote d’imprimante GDI.</span><span class="sxs-lookup"><span data-stu-id="d9d2d-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="d9d2d-108">Pour obtenir une description des événements de document du pilote d’imprimante GDI, consultez [fonction DocumentEvent](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="d9d2d-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9d2d-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9d2d-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9d2d-110">Utilisation de l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d9d2d-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="d9d2d-111">Informations de référence sur l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d9d2d-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
