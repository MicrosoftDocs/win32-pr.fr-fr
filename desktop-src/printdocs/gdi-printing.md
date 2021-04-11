---
description: L’API d’impression GDI fournit des applications avec une interface d’impression indépendante du périphérique.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API d’impression GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202812"
---
# <a name="gdi-print-api"></a><span data-ttu-id="5e37b-103">API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="5e37b-103">GDI Print API</span></span>

<span data-ttu-id="5e37b-104">L’API d’impression GDI fournit des applications avec une interface d’impression indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="5e37b-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="5e37b-105">Utilisez cette interface si l’application utilise GDI pour afficher du texte et des graphiques.</span><span class="sxs-lookup"><span data-stu-id="5e37b-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="5e37b-106">Si vous écrivez des applications pour Windows Vista ou des versions ultérieures de Windows, envisagez d’utiliser l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) et l' [API d’impression XPS](xps-printing.md) pour utiliser les interfaces graphiques de performances supérieures prises en charge par les pilotes d’impression XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="5e37b-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="5e37b-107">Cette section fournit des informations sur les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="5e37b-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="5e37b-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="5e37b-108">Topic</span></span>                                                                                             | <span data-ttu-id="5e37b-109">Description</span><span class="sxs-lookup"><span data-stu-id="5e37b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e37b-110">À propos de l’API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="5e37b-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="5e37b-111">Vue d’ensemble de la fonctionnalité d’impression GDI.</span><span class="sxs-lookup"><span data-stu-id="5e37b-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="5e37b-112">Utilisation de l’API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="5e37b-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="5e37b-113">Informations sur l’utilisation de l’API d’impression GDI dans une application.</span><span class="sxs-lookup"><span data-stu-id="5e37b-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="5e37b-114">Référence de l’API d’impression GDI</span><span class="sxs-lookup"><span data-stu-id="5e37b-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="5e37b-115">Description détaillée des fonctions, structures et autres éléments de l’API d’impression GDI.</span><span class="sxs-lookup"><span data-stu-id="5e37b-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="5e37b-116">Microsoft XPS Document Converter (MXDC)</span><span class="sxs-lookup"><span data-stu-id="5e37b-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="5e37b-117">[Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) est un composant qui permet aux applications d’utiliser l’API d’impression GDI avec les imprimantes qui ont un pilote d’impression XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="5e37b-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="5e37b-118">Microsoft XPS document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="5e37b-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="5e37b-119">[Microsoft XPS document Writer (MXDW)](microsoft-xps-document-writer.md) fournit des applications avec la fonctionnalité « enregistrer en tant que XPS » ou « exporter vers XPS ».</span><span class="sxs-lookup"><span data-stu-id="5e37b-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="5e37b-120">Les applications qui ne créent pas de contenu de document XPS en mode natif peuvent utiliser le MXDW pour créer des fichiers de document XPS sans utiliser l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e37b-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="5e37b-121">Toutefois, l’API de document XPS offre à une application la possibilité d’utiliser les interfaces graphiques de performances supérieures prises en charge par les pilotes d’impression XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="5e37b-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="5e37b-122">Le diagramme suivant montre la relation entre l’API d’impression GDI et les autres API d’impression qu’une application peut utiliser.</span><span class="sxs-lookup"><span data-stu-id="5e37b-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![diagramme qui montre la relation entre l’API d’impression GDI et les autres API d’impression qu’une application Win32 peut utiliser](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="5e37b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e37b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e37b-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="5e37b-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="5e37b-126">[API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5e37b-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5e37b-127">API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="5e37b-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="5e37b-128">API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="5e37b-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="5e37b-129">API ticket d’impression</span><span class="sxs-lookup"><span data-stu-id="5e37b-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

