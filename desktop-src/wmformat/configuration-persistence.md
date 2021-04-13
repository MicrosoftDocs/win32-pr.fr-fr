---
title: Persistance de la configuration
description: Persistance de la configuration
ms.assetid: 0ef1a0a1-767d-4f34-91d8-9d15c46f3954
keywords:
- Windows Media Format SDK, persistance
- Windows Media Format SDK, persistance de configuration
- Format de systèmes avancés (ASF), persistance
- ASF (format des systèmes avancés), persistance
- Format de systèmes avancés (ASF), persistance de configuration
- ASF (format de systèmes avancés), persistance de configuration
- persistance de la configuration
- persistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3707c82ff9d7ce6821ad33e83b158c11b5a9030c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381561"
---
# <a name="configuration-persistence"></a>Persistance de la configuration

Aucune des propriétés activées en écriture décrites dans cette documentation n’est enregistrée par le kit de développement logiciel (SDK) Windows Media. Chaque application qui utilise le kit de développement logiciel (SDK) doit fournir ses propres procédures de persistance en fonction des besoins et appeler la méthode Set appropriée sur chaque instance du kit de développement logiciel (SDK). De cette façon, les modifications de configuration apportées par une application n’affectent pas une autre application. Par exemple, la modification du temps de mise en mémoire tampon dans un joueur n’affecte pas un autre lecteur.

La seule exception à cette règle concerne les informations d’identification. Si l’application indique, dans son retour de l’appel **AcquireCredentials** , que les informations d’ID d’utilisateur et de mot de passe doivent être persistantes, le kit de développement logiciel (SDK) enregistre ces informations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Implémentation des fonctionnalités réseau**](implementing-network-functionality.md)
</dt> <dt>

[**Interface IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> </dl>

 

 




