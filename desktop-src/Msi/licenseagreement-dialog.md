---
description: Cette boîte de dialogue modale affiche le contrat de licence pour l’utilisateur.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Boîte de dialogue LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011972"
---
# <a name="licenseagreement-dialog"></a>Boîte de dialogue LicenseAgreement

Cette boîte de dialogue modale affiche le contrat de licence pour l’utilisateur. En général, la boîte de dialogue affiche le texte de l’accord à l’aide d’un [contrôle ScrollableText](scrollabletext-control.md) et d’une paire de cases d’option qui permettent à l’utilisateur d’accepter ou de refuser le contrat. Pour des raisons juridiques, il est recommandé qu’aucun bouton ne soit présenté à l’utilisateur, comme déjà sélectionné par défaut. Cela oblige l’utilisateur à faire un choix actif. Les auteurs utilisent généralement un [contrôle RadioButtonGroup](radiobuttongroup-control.md) à cet effet. Notez cependant que le focus sur une boîte de dialogue n’est pas déplacé vers un contrôle RadioButtonGroup tant que l’un des boutons du groupe n’a pas été sélectionné.

 

 



