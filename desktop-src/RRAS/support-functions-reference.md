---
title: Référence des fonctions de prise en charge
description: Les fonctions suivantes sont fournies aux protocoles de routage par le gestionnaire de routeur.
ms.assetid: 4e88c9fe-f6ec-4f9c-88b1-8726e10d0f6d
keywords:
- Routage de l’interface de protocole RRAS, fonctions de prise en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbaba49c5f7e4130491a50176d560ee565b0046
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463494"
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

 

 