---
description: Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Définition d’un niveau d’authentification pour une application serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6248574117a55420940fbaf24f88c5d3b2c8721e6fa022bad5923ba658bf5da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546253"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Définition d’un niveau d’authentification pour une application serveur

Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application. Les niveaux d’authentification plus élevés fournissent une sécurité et une intégrité des données accrues, bien qu’ils entraînent généralement une dégradation des performances. Pour plus d’informations, consultez [authentification du client](client-authentication.md).

**Pour sélectionner un niveau d’authentification pour une application serveur**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous configurez l’authentification, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Dans la zone **niveau d’authentification pour les appels** , sélectionnez le niveau approprié. Les niveaux sont les suivants, triés de la sécurité la plus faible à la plus élevée :

    -   **Aucun**. Aucune authentification n’est effectuée.
    -   **Connecter**. Authentifie les informations d'identification uniquement lorsque la connexion est établie.
    -   **Appelez**. Authentifie les informations d'identification au début de chaque appel.
    -   **Paquet**. Authentifie les informations d'identification et vérifie que toutes les données d'appel sont reçues. Il s’agit du paramètre par défaut pour les applications serveur COM+.
    -   **Intégrité des paquets**. Authentifie les informations d'identification et vérifie qu'aucune donnée d'appel n'a été modifiée lors du transit.
    -   **Confidentialité du paquet**. Authentifie les informations d'identification et chiffre le paquet, y compris les données et l'identité et la signature de l'expéditeur.

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



