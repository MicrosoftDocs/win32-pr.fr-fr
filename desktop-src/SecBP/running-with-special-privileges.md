---
description: Certaines fonctions requièrent des privilèges spéciaux pour s’exécuter correctement.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Exécution avec des privilèges spéciaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9bcd9db0f54c14c5a66d452e394252e6dacad933a92157f59811af90f84a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127269"
---
# <a name="running-with-special-privileges"></a>Exécution avec des privilèges spéciaux

Certaines fonctions requièrent [des privilèges](/windows/desktop/SecAuthZ/privileges) spéciaux pour s’exécuter correctement. Dans certains cas, la fonction ne peut être exécutée que par certains utilisateurs ou par les membres de certains groupes. L’exigence la plus courante est que l’utilisateur soit un administrateur local. D’autres fonctions requièrent que le compte de l’utilisateur ait des privilèges spécifiques activés.

Pour réduire le risque que du code non autorisé soit en mesure d’accéder au contrôle, le système doit s’exécuter avec les privilèges minimum nécessaires. Les applications qui doivent appeler des fonctions qui requièrent des privilèges spéciaux peuvent faire en sorte que le système soit ouvert aux attaques de pirates. Ces applications doivent être conçues pour s’exécuter pendant de courtes périodes et doivent informer l’utilisateur des implications en matière de sécurité.

Pour plus d’informations sur l’exécution de en tant qu’utilisateur différent et sur l’activation des privilèges dans votre application, consultez les rubriques suivantes :<dl>

[Exécution avec des privilèges d’administrateur](running-with-administrator-privileges.md)  
[Demande d’informations d’identification à l’utilisateur](asking-the-user-for-credentials.md)  
[Modification des privilèges dans un jeton](changing-privileges-in-a-token.md)  
[Attribution de privilèges à un compte](assigning-privileges-to-an-account.md)  
</dl>

 

 
