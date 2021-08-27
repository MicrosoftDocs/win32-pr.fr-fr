---
title: Référence des fonctions de prise en charge
description: Les fonctions suivantes sont fournies aux protocoles de routage par le gestionnaire de routeur.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Routage de l’interface de protocole RRAS, fonctions de prise en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa2af1b38e88e9f3b7a55e8026ad42f4b1d0cff26de3798fb04621a1288ad9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073709"
---
# <a name="support-functions-reference"></a>Référence des fonctions de prise en charge

Les fonctions suivantes sont fournies aux protocoles de routage par le gestionnaire de routeur. Lorsque le gestionnaire de routeur appelle la fonction [**StartProtocol**](/windows/desktop/api/Routprot/nc-routprot-pstart_protocol) (implémentée par le protocole de routage), le gestionnaire de routeur transmet au protocole de routage une structure de [**\_ fonctions de prise en charge**](/windows/desktop/api/Routprot/ns-routprot-support_functions_50) contenant des pointeurs vers ces fonctions :

[**DemandDialRequest**](/previous-versions/windows/desktop/legacy/aa373924(v=vs.85))

[**MIBEntryCreate**](/previous-versions/windows/desktop/legacy/aa374538(v=vs.85))

[**MIBEntryDelete**](/previous-versions/windows/desktop/legacy/aa374539(v=vs.85))

[**MIBEntryGet**](/previous-versions/windows/desktop/legacy/aa374540(v=vs.85))

[**MIBEntryGetFirst**](/previous-versions/windows/desktop/legacy/aa374541(v=vs.85))

[**MIBEntryGetNext**](/previous-versions/windows/desktop/legacy/aa374542(v=vs.85))

[**MIBEntrySet**](/previous-versions/windows/desktop/legacy/aa374543(v=vs.85))

[**SetInterfaceReceiveType**](/previous-versions/windows/desktop/legacy/aa382181(v=vs.85))

[**ValidateRoute**](/previous-versions/windows/desktop/legacy/aa382342(v=vs.85))

 

 