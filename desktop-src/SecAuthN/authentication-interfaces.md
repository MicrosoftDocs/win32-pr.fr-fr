---
description: Répertorie les interfaces dans les API d’authentification.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843385004095499a59593bf548ff21998c4079e48667ea0e472e4a55d1f57ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141402"
---
# <a name="authentication-interfaces"></a>Interfaces d’authentification

Les interfaces d’authentification sont classées en fonction de l’utilisation comme suit :

-   [Interfaces de carte à puce](#smart-card-interfaces)
-   [Interfaces de partage d’identité](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a>Interfaces de carte à puce

Le kit de développement logiciel (SDK) de carte à puce fournit les interfaces COM suivantes. Les méthodes pour une interface spécifique sont répertoriées dans la table des matières et dans la page de référence de cette interface.



| Interface                                    | Description                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IByteBuffer**](ibytebuffer.md)           | Gère un objet de flux.                                                                                                                                                                 |
| [**ISCard**](iscard.md)                     | Ouvre et gère une connexion à une [*carte à puce*](/windows/desktop/SecGloss/s-gly).                                                                    |
| [**ISCardAuth**](iscardauth.md)             | Authentifie une application, une carte à puce ou un utilisateur.                                                                                                                                       |
| [**ISCardCmd**](iscardcmd.md)               | Construit et gère une [*unité de données de protocole d’application*](/windows/desktop/SecGloss/a-gly) de carte à puce (APDU). |
| [**ISCardDatabase**](iscarddatabase.md)     | Effectue les opérations de base de données du [*Gestionnaire de ressources*](/windows/desktop/SecGloss/r-gly) de carte à puce.                                              |
| [**ISCardFileAccess**](iscardfileaccess.md) | Exécute des services de fichiers communs tels que la localisation, la sélection, la lecture, l’écriture, la création et la suppression de fichiers.                                                                               |
| [**ISCardISO7816**](iscardiso7816.md)       | Construit une commande APDU.                                                                                                                                                              |
| [**ISCardLocate**](iscardlocate.md)         | Localise une carte à puce.                                                                                                                                                                    |
| [**ISCardManage**](iscardmanage.md)         | Gère le système de carte à puce.                                                                                                                                                           |
| [**ISCardTypeConv**](iscardtypeconv.md)     | Fournit des méthodes utilisées pour prendre en charge d’autres interfaces COM de carte à puce. Cette interface n’est fournie qu’à des fins de compatibilité descendante et ne doit plus être utilisée.                               |
| [**ISCardVerify**](iscardverify.md)         | Vérifie ou modifie la stratégie de vérification des titulaires de cartes (IVT).                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a>Interfaces de partage d’identité

Le kit de développement logiciel (SDK) partage d’identité fournit les interfaces COM suivantes. Les méthodes pour une interface spécifique sont répertoriées dans la table des matières et dans la page de référence de cette interface.



| Interface                                                          | Description                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**IAssociatedIdentityProvider**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | Permet à un fournisseur d’identité d’associer des identités à des comptes d’utilisateurs locaux.            |
| [**IIdentityAdvise**](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | Permet à un fournisseur d’identité de notifier une application appelante lorsqu’une identité est mise à jour. |
| [**IIdentityProvider**](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | Représente un fournisseur d'identité.                                                         |
| [**IIdentityStore**](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | Fournit des méthodes pour énumérer et gérer des identités et des fournisseurs d’identité.              |



 

 

 
