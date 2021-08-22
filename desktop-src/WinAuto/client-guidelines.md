---
title: Instructions du client
description: Les développeurs clients doivent utiliser les fonctionnalités suivantes pour obtenir des informations sur les éléments de l’interface utilisateur
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133942"
---
# <a name="client-guidelines"></a>Instructions du client

Les développeurs clients doivent utiliser les fonctionnalités suivantes pour obtenir des informations sur les éléments de l’interface utilisateur :

-   Pour récupérer une interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) aux objets, appelez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Pour examiner et manipuler des objets accessibles, utilisez les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
-   Pour recevoir [winEvents](winevents-overview.md), appelez [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) pour inscrire une fonction de rappel WinEvent pour les événements pertinents pour l’application cliente.

## <a name="in-this-section"></a>Dans cette section

-   [Obtention des ID enfants par les clients](how-clients-obtain-child-ids.md)

 

 




