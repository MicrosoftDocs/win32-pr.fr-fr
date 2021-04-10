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
# <a name="wia-property-validation"></a>Validation de la propriété WIA

Quand une application exécute une opération [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) sur une propriété WIA (Windows Image Acquisition) accessible en écriture, le pilote WIA effectue une validation sur la nouvelle valeur de propriété. L’écriture d’une propriété peut avoir des effets secondaires qui modifient d’autres valeurs de propriété. Il revient à l’application de lire toutes les valeurs de propriété après une opération d’écriture pour déterminer que toutes les propriétés sont définies sur les valeurs souhaitées par l’application.

Plusieurs propriétés peuvent être écrites simultanément à l’aide de l’opération [IPropertyStorage :: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) . Il peut y avoir des cas où certaines assignations de propriété sont en conflit. Dans ce cas, la priorité utilisée pour résoudre les conflits est la suivante :

1.  Intent IPS de WIA \_ \_ \_
2.  type de données WIA de la \_ Loi WIA \_
3.  profondeur WIA de la \_ Loi WIA \_
4.  \_XRES IPS \_ WIA
5.  \_YRES IPS \_ WIA
6.  \_adresses IP WIA, \_ xpos
7.  \_Posy IPS \_ WIA
8.  \_XEXTENT IPS \_ WIA
9.  \_YEXTENT IPS \_ WIA

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
