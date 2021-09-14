---
description: Les constantes suivantes peuvent être retournées en tant qu’erreurs.
ms.assetid: 185bd906-c276-4075-9c23-eb112da2a7ca
title: Constantes RND_ (Rnderr. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a89b6747fb9fef775bbf40fac472081567ff1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414686"
---
# <a name="rnd_-constants"></a>RND, \_ constantes

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Les constantes suivantes peuvent être retournées en tant qu’erreurs.

<dl> <dt>

<span id="RND_INVALID_TIME"></span><span id="rnd_invalid_time"></span>**\_durée non valide de RND \_**
</dt> <dd> <dl> <dt>

 0xe0000200
</dt> <dt>



La valeur d’heure entrée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="RND_NULL_SERVER_NAME"></span><span id="rnd_null_server_name"></span>**nom du serveur de RND \_ null \_ \_**
</dt> <dd> <dl> <dt>

 0xe0000201
</dt> <dt>



Le nom du serveur est **null**, probablement parce que [**ITConferenceBlob :: init**](itconferenceblob-init.md) n’a pas été exécuté ou n’a pas réussi.


</dt> </dl> </dd> <dt>

<span id="RND_ALREADY_CONNECTED"></span><span id="rnd_already_connected"></span>**RND \_ déjà \_ connecté**
</dt> <dd> <dl> <dt>

 0xe0000202
</dt> <dt>



la méthode [**ITDirectory :: Connecter**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) a été appelée, mais une connexion existe déjà.


</dt> </dl> </dd> <dt>

<span id="RND_NOT_CONNECTED"></span><span id="rnd_not_connected"></span>**RND \_ non \_ connecté**
</dt> <dd> <dl> <dt>

 0xe0000203
</dt> <dt>



la méthode [**ITDirectory :: Connecter**](/windows/desktop/api/Rend/nf-rend-itdirectory-connect) n’a pas été appelée ou a échoué.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                               |
| En-tête<br/>       | <dl> <dt>Rnderr. h</dt> </dl> |



 

 




