---
description: Le protocole PGM utilise des options de socket pour définir l’État, fournir des paramètres de multidiffusion et, sinon, implémenter ses fonctionnalités de multidiffusion.
ms.assetid: 91f5b051-cc42-46ba-88d9-680bd0367aff
title: Options de socket PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e8df8050146774ac79d45594adcccf53a93d295ce42b9f00834aa0d699e83a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860819"
---
# <a name="pgm-socket-options"></a>Options de socket PGM

Le protocole PGM utilise des options de socket pour définir l’État, fournir des paramètres de multidiffusion et, sinon, implémenter ses fonctionnalités de multidiffusion. Cette page spécifie la manière dont les options de socket PGM doivent être définies, énumère les options de Socket disponibles pour le protocole PGM et, le cas échéant, fournit des exemples d’utilisation et des informations supplémentaires pour diverses options. Pour obtenir les définitions de base de chaque option de socket PCM, consultez [options de socket](socket-options.md).

**Windows XP :** La programmation de la multidiffusion (PGM) fiable n’est pas prise en charge.

Les options de socket suivantes sont disponibles pour les expéditeurs PGM :

<dl> \_LATEJOIN RM  
taille de la \_ fenêtre de tarif RM \_ \_  
taux d’avancée de la \_ fenêtre d’envoi RM \_ \_ \_  
\_statistiques des expéditeurs RM \_  
\_ \_ \_ méthode avancée de la fenêtre d’expéditeur RM \_  
RM \_ Set \_ MCAST \_ TTL  
configuration de la \_ \_ limite du message RM \_  
RM- \_ définir \_ Envoyer \_ si  
RM \_ utiliser \_ FEC  
</dl>

L’option de méthode Advance de la fenêtre de l' \_ expéditeur RM \_ \_ \_ spécifie la méthode utilisée lors de l’avancement de la fenêtre d’envoi du bord de fin. Le paramètre optval peut uniquement être une \_ fenêtre \_ Advance \_ par \_ heure (valeur par défaut). Notez que l' \_ \_ utilisation \_ du cache de données par la fenêtre E \_ \_ n’est pas prise en charge.

Les options de socket suivantes sont disponibles pour les récepteurs PGM :

<dl> RM- \_ Ajouter une \_ réception \_ si  
\_réception RM \_ del \_ si  
\_ \_ abonnement intranet à vitesse élevée \_ RM \_  
\_statistiques du récepteur RM \_  
</dl>

## <a name="setting-pgm-socket-options"></a>Définition des options de socket PGM

L’extrait de code suivant illustre une règle de programmation pour définir les options de socket PGM :


```C++

ULONG       OptionData;    // This structure is option-dependent
//     :
setsockopt (s,
            IPPROTO_RM,
            Socket_Option,
            (char *) &OptionData,
            sizeof (OptionData));


```



Dans l’extrait de code ci-dessus, le type et le contenu de l’objet de contenu sont dépendants de l' *option de socket* définie. Pour toutes les options de socket PGM, le niveau de socket est IPPROTO \_ RM. Les options de socket PGM doivent être définies immédiatement après l’appel à la fonction [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) , avec les exceptions suivantes :

<dl> configuration de la \_ \_ limite du message RM \_  
\_statistiques des expéditeurs RM \_  
\_statistiques du récepteur RM \_  
</dl>

 

 



