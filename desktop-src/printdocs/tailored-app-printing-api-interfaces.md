---
description: Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimer les interfaces API des packages de documents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535553"
---
# <a name="print-document-package-api-interfaces"></a><span data-ttu-id="58fa9-103">Imprimer les interfaces API des packages de documents</span><span class="sxs-lookup"><span data-stu-id="58fa9-103">Print Document Package API Interfaces</span></span>

<span data-ttu-id="58fa9-104">Les interfaces suivantes sont utilisées par une application pour gérer le package de document d’impression.</span><span class="sxs-lookup"><span data-stu-id="58fa9-104">The following interfaces are used by an app to manage the print document package.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58fa9-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="58fa9-105">In this section</span></span>



| <span data-ttu-id="58fa9-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="58fa9-106">Topic</span></span>                                                                                       | <span data-ttu-id="58fa9-107">Description</span><span class="sxs-lookup"><span data-stu-id="58fa9-107">Description</span></span>                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58fa9-108">**IPrintDocumentPackageStatusEvent**</span><span class="sxs-lookup"><span data-stu-id="58fa9-108">**IPrintDocumentPackageStatusEvent**</span></span>](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | <span data-ttu-id="58fa9-109">Représente la progression du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="58fa9-109">Represents the progress of the print job.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="58fa9-110">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="58fa9-110">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | <span data-ttu-id="58fa9-111">Permet aux utilisateurs d’énumérer les types de cibles de package pris en charge et d’en créer un avec un ID de type donné.</span><span class="sxs-lookup"><span data-stu-id="58fa9-111">Allows users to enumerate the supported package target types and to create one with a given type ID.</span></span> <span data-ttu-id="58fa9-112">**IPrintDocumentPackageTarget** prend également en charge le suivi de la progression et de l’annulation de l’impression du package.</span><span class="sxs-lookup"><span data-stu-id="58fa9-112">**IPrintDocumentPackageTarget** also supports the tracking of the package printing progress and cancelling.</span></span><br/> |
| [<span data-ttu-id="58fa9-113">**IPrintDocumentPackageTargetFactory**</span><span class="sxs-lookup"><span data-stu-id="58fa9-113">**IPrintDocumentPackageTargetFactory**</span></span>](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | <span data-ttu-id="58fa9-114">Utilisé avec [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) pour démarrer un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="58fa9-114">Used with [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for starting a print job.</span></span><br/>                                                                                                               |



 

 

