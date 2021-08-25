---
title: Exemple de diagnostics NDF
description: L’exemple suivant montre comment lancer l’interface utilisateur NDF et diagnostiquer la connectivité au site Web http//www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa1971da12b7d707dc74b34497dff630ee8fdd8f93d5737ae3757bdde129fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802369"
---
# <a name="ndf-diagnostics-example"></a>Exemple de diagnostics NDF

L’exemple suivant montre comment lancer l’interface utilisateur NDF et diagnostiquer la connectivité au site Web https://www.microsoft.com .


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



L’interface utilisateur NDF peut être lancée sous la forme d’une fenêtre modale. Pour ce faire, remplacez le deuxième paramètre de [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) par **null** par le handle (HWND) de la fenêtre parente.

Cet exemple peut être modifié pour diagnostiquer d’autres zones de la mise en réseau. Pour ce faire, remplacez l’appel [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) par l’une des autres fonctions de création d’incident, telles que [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) ou [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




