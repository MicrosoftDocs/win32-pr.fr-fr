---
title: Interfaces dans les objets distribués
description: Dans l’informatique distribuée, une interface est une collection de définitions et de fonctions distantes qui permettent à plusieurs programmes d’interagir entre différents contextes.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfaces MIDL, dans les objets distribués
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8661e7e07f08d35151afe8fb256539ed574b0a0162178e3a9e63dc8c43c59ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807136"
---
# <a name="interfaces-in-distributed-objects"></a>Interfaces dans les objets distribués

Dans l’informatique distribuée, une interface est une collection de définitions et de fonctions distantes qui permettent à plusieurs programmes d’interagir entre différents contextes. Dans une application RPC, une interface spécifie les éléments suivants :

-   Comment les applications client et serveur s’identifient les unes avec les autres.
-   Mode de transmission des données entre le client et le serveur.
-   Procédures distantes que l’application cliente peut appeler.
-   Types de données pour les paramètres et les valeurs de retour des procédures distantes.

Le Microsoft Interface Definition Language (MIDL) est destiné à l’implémentation des interfaces utilisées dans les applications distribuées. Avec MIDL, une application peut avoir une interface ou plusieurs. Chaque interface spécifie un contrat distribué unique entre les programmes client et serveur. Les applications basées sur des appels de procédure distante (RPC), COM (Component Object Model) et DCOM (Distributed Component Object Model) spécifient leurs interfaces à l’aide de MIDL.

MIDL ressemble à C et C++ de nombreuses façons. Pour obtenir une vue d’ensemble de l’écriture d’interfaces MIDL, consultez [développement de l’interface](/windows/desktop/Rpc/developing-the-interface).

 

 