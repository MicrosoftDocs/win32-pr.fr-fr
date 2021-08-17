---
description: Un utilisateur peut vérifier l’état de l’interface Teredo à partir de l’invite de commandes en tapant netsh interface teredo show State et en examinant la sortie.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: L’infrastructure homologue et Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18dfa3fe075d0829358849b3783272aac74e60545c1e58e1d9bf1663738e3721
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794236"
---
# <a name="the-peer-infrastructure-and-teredo"></a>L’infrastructure homologue et Teredo

Un utilisateur peut vérifier l’état de l’interface [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) à partir de l’invite de commandes en tapant **netsh interface teredo show State** et en examinant la sortie. Si l’État est « hors connexion », Teredo n’est pas actif, ce qui empêche l’utilisateur de se connecter à d’autres utilisateurs via leurs adresses Teredo. Il est possible que Teredo soit hors connexion, car votre pare-feu est désactivé ou ne prend pas en charge [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).

 

 
