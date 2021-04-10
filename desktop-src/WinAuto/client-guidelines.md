---
title: Instructions du client
description: Les développeurs clients doivent utiliser les fonctionnalités suivantes pour obtenir des informations sur les éléments de l’interface utilisateur
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103940631"
---
# <a name="client-guidelines"></a><span data-ttu-id="18f94-103">Instructions du client</span><span class="sxs-lookup"><span data-stu-id="18f94-103">Client Guidelines</span></span>

<span data-ttu-id="18f94-104">Les développeurs clients doivent utiliser les fonctionnalités suivantes pour obtenir des informations sur les éléments de l’interface utilisateur :</span><span class="sxs-lookup"><span data-stu-id="18f94-104">Client developers should use the following functionality to get information about the user interface elements:</span></span>

-   <span data-ttu-id="18f94-105">Pour récupérer une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aux objets, appelez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="18f94-105">To get an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface to objects, call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), or [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>
-   <span data-ttu-id="18f94-106">Pour examiner et manipuler des objets accessibles, utilisez les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="18f94-106">To examine and manipulate accessible objects, use the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods.</span></span>
-   <span data-ttu-id="18f94-107">Pour recevoir [winEvents](winevents-overview.md), appelez [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) pour inscrire une fonction de rappel WinEvent pour les événements pertinents pour l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="18f94-107">To receive [WinEvents](winevents-overview.md), call [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) to register a WinEvent callback function for those events that are relevant to the client application.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="18f94-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="18f94-108">In this section</span></span>

-   [<span data-ttu-id="18f94-109">Obtention des ID enfants par les clients</span><span class="sxs-lookup"><span data-stu-id="18f94-109">How Clients Obtain Child IDs</span></span>](how-clients-obtain-child-ids.md)

 

 




