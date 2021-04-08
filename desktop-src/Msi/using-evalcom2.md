---
description: Evalcom2.dll peut être utilisé pour implémenter des opérations de validation pour des packages d’installation et des modules de fusion à l’aide d’évaluateurs de cohérence internes-ICEs.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Utilisation de Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751693"
---
# <a name="using-evalcom2"></a>Utilisation de Evalcom2

Evalcom2.dll peut être utilisé pour implémenter des opérations de validation pour des packages d’installation et des modules de fusion à l’aide d' [évaluateurs de cohérence internes-ICEs](internal-consistency-evaluators-ices.md). L’objet principal implémente des interfaces pour les programmes C/C++.

L’objet principal implémente également des [interfaces Evalcom2](evalcom2-interfaces.md) pour les programmes C/C++. Le CLSID requis pour obtenir l’interface à partir de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) est {6E5E1910-8053-4660-B795-6B612E29BC58}. REFIID est {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Vous pouvez utiliser la procédure suivante pour implémenter des opérations de validation.

**Pour implémenter des opérations de validation**

1.  Initialisez COM sur le thread appelant à l’aide de [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Obtenez le pointeur vers l’interface [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) à l’aide de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Ouvrez le package d’installation ou le module de fusion à l’aide de la méthode [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .
4.  Ouvrez le fichier d’évaluation à l’aide de la méthode [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .
5.  Définissez la fonction de rappel d’affichage à l’aide de la méthode [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .
6.  Définissez la fonction de rappel d’État à l’aide de la méthode [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .
7.  Effectuez la validation à l’aide de la méthode [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .
8.  Fermez le fichier. CUB à l’aide de la méthode [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .
9.  Fermez la base de données à l’aide de la méthode [**FermerBase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .
10. Libérez l’interface [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .
11. Désinitialisez COM à l’aide de [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces Evalcom2](evalcom2-interfaces.md)
</dt> <dt>

[Automation de validation](validation-automation.md)
</dt> <dt>

[Fonctions de rappel de validation](validation-callback-functions.md)
</dt> </dl>

 

 
