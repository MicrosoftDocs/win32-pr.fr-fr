---
title: Prise en charge du langage XML
description: Cette section décrit le niveau de prise en charge du langage XML dans WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Services Web de prise en charge du langage XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106512533"
---
# <a name="xml-language-support"></a><span data-ttu-id="046b1-106">Prise en charge du langage XML</span><span class="sxs-lookup"><span data-stu-id="046b1-106">XML Language Support</span></span>

<span data-ttu-id="046b1-107">Cette section décrit le niveau de prise en charge du langage XML dans WWS.</span><span class="sxs-lookup"><span data-stu-id="046b1-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="046b1-108">Consultez les fonctions DownlevelLCIDToLocaleName sur les versions de Windows antérieures à Windows Vista, et LCIDToLocalName dans le cas contraire, pour effectuer une conversion entre un LCID et une valeur XML : lang.</span><span class="sxs-lookup"><span data-stu-id="046b1-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="046b1-109">Lors de la lecture, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) peut être utilisé pour découvrir la valeur d’un attribut « XML : lang » dans la portée.</span><span class="sxs-lookup"><span data-stu-id="046b1-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="046b1-110">Lors de l’écriture, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) peut être utilisé pour écrire un attribut "XML : lang".</span><span class="sxs-lookup"><span data-stu-id="046b1-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




