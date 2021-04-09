---
description: Les fonctions de configuration de modem vous permettent de configurer un modem avant d’établir une connexion.
ms.assetid: 67d8f3c4-0295-4028-8b12-1a5e26979df5
title: Configuration du modem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7abd6c5319011b8821487b6adf0351dc799e61f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861477"
---
# <a name="modem-configuration"></a>Configuration du modem

Les fonctions de configuration de modem vous permettent de configurer un modem avant d’établir une connexion. Une application peut définir des options de modem et déterminer les fonctionnalités d’un modem sans utiliser de commandes spécifiques à un périphérique modem. Voici les fonctionnalités générales qu’une application peut définir avant d’effectuer un appel :

-   Mode d’opération principal (synchrone, asynchrone et si le contrôle d’erreur est activé).
-   V. 42 contrôle d’erreur (défini par la recommandation CCITT V. 42), y compris les paramètres spécifiques. CCITT correspond au Comité consultatif international pour les télégraphiques et les téléphones.
-   V. 42bis (défini par la recommandation CCITT V. 42bis) et la compression de données MNP5.
-   Options de délai d’attente, notamment la configuration des appels, l’inactivité et la remise des données mises en mémoire tampon.

Avant de définir la configuration d’un modem, une application doit déterminer les fonctionnalités du périphérique modem à l’aide de la fonction [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties) . Cette fonction remplit une structure [**COMMPROP**](/windows/desktop/api/WinBase/ns-winbase-commprop) . Cette structure contient à la fois une partie générale, qui s’applique à tous les appareils de communication et une partie spécifique à chaque sous-type de fournisseur. Pour les périphériques à modems, la partie spécifique au fournisseur de la structure **COMMPROP** est une structure [**MODEMDEVCAPS**](/windows/desktop/api/Mcx/ns-mcx-modemdevcaps) .

Une application peut obtenir et définir la configuration actuelle d’un modem à l’aide des fonctions [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig) et [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig) , qui utilisent toutes les deux une structure [**COMMCONFIG**](/windows/desktop/api/Winbase/ns-winbase-commconfig) . Cette structure contient à la fois une partie générale, qui s’applique à tous les appareils de communication et une partie spécifique à chaque sous-type de fournisseur. Pour les périphériques à modems, la partie spécifique au fournisseur de la structure **COMMCONFIG** est une structure [**MODEMSETTINGS**](/windows/desktop/api/Mcx/ns-mcx-modemsettings) .

Après la configuration d’un modem, une application peut utiliser l’interface de programmation d’applications de téléphonie (TAPI) pour établir une connexion.

Les fonctions de configuration du modem ne permettent pas la gestion et la maintenance à long terme d’un modem. Les fournisseurs de services de modem doivent fournir des boîtes de dialogue de configuration de modem à cet effet.

 

 



