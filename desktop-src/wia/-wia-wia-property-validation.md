---
description: 'Quand une application exécute une opération IPropertyStorage :: WriteMultiple sur une propriété WIA (Windows Image Acquisition) accessible en écriture, le pilote WIA effectue une validation sur la nouvelle valeur de propriété.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validation de la propriété WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201478"
---
# <a name="wia-property-validation"></a><span data-ttu-id="9a5b6-103">Validation de la propriété WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-103">WIA Property Validation</span></span>

<span data-ttu-id="9a5b6-104">Quand une application exécute une opération [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) sur une propriété WIA (Windows Image Acquisition) accessible en écriture, le pilote WIA effectue une validation sur la nouvelle valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="9a5b6-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="9a5b6-105">L’écriture d’une propriété peut avoir des effets secondaires qui modifient d’autres valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="9a5b6-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="9a5b6-106">Il revient à l’application de lire toutes les valeurs de propriété après une opération d’écriture pour déterminer que toutes les propriétés sont définies sur les valeurs souhaitées par l’application.</span><span class="sxs-lookup"><span data-stu-id="9a5b6-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="9a5b6-107">Plusieurs propriétés peuvent être écrites simultanément à l’aide de l’opération [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) .</span><span class="sxs-lookup"><span data-stu-id="9a5b6-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="9a5b6-108">Il peut y avoir des cas où certaines assignations de propriété sont en conflit.</span><span class="sxs-lookup"><span data-stu-id="9a5b6-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="9a5b6-109">Dans ce cas, la priorité utilisée pour résoudre les conflits est la suivante :</span><span class="sxs-lookup"><span data-stu-id="9a5b6-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="9a5b6-110">Intent IPS de WIA \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="9a5b6-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="9a5b6-111">type de données WIA de la \_ Loi WIA \_</span><span class="sxs-lookup"><span data-stu-id="9a5b6-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="9a5b6-112">profondeur WIA de la \_ Loi WIA \_</span><span class="sxs-lookup"><span data-stu-id="9a5b6-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="9a5b6-113">\_XRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="9a5b6-114">\_YRES IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="9a5b6-115">\_adresses IP WIA, \_ xpos</span><span class="sxs-lookup"><span data-stu-id="9a5b6-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="9a5b6-116">\_Posy IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="9a5b6-117">\_XEXTENT IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="9a5b6-118">\_YEXTENT IPS \_ WIA</span><span class="sxs-lookup"><span data-stu-id="9a5b6-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a5b6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a5b6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5b6-120">**IWiaPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="9a5b6-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
