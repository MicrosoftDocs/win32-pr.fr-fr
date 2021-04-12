---
title: Méthode SetInfo
description: La méthode IADs SetInfo enregistre les valeurs actuelles des propriétés de cet objet Active Directory depuis le cache des propriétés vers le magasin d’annuaires sous-jacent. Cela est similaire au vidage d’une mémoire tampon sur le disque.
ms.assetid: e4152b3d-3a59-4f69-9765-03cdf6286459
ms.tgt_platform: multiple
keywords:
- SetInfo ADSI, utilisation
- propriétés ADSI, enregistrer les valeurs actuelles des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5965a46e5accd2a00adc006fe37511de13ff0df3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309214"
---
# <a name="the-setinfo-method"></a>Méthode SetInfo

La méthode [**IADs :: setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) enregistre les valeurs actuelles des propriétés de cet objet Active Directory depuis le cache des propriétés vers le magasin d’annuaires sous-jacent. Cela est similaire au vidage d’une mémoire tampon sur le disque.

[**Setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) met à jour les objets qui existent déjà dans l’annuaire, ou crée une entrée d’annuaire pour les objets nouvellement créés.

Au moment de l’appel de [**setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , si des valeurs de cache de propriété ont été écrites [**avec un code de contrôle**](/windows/desktop/api/Iads/nf-iads-iads-putex) de point de contrôle d’état de la propriété, par exemple, \_ \_ la propriété ad Update ou ADS est \_ \_ désactivée, les demandes appropriées sont transmises au service d’annuaire sous-jacent.

 

 




