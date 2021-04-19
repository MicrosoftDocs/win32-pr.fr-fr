---
description: Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Définition d’un niveau d’authentification pour une application serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512897"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a>Définition d’un niveau d’authentification pour une application serveur

Lorsque vous définissez un niveau d’authentification pour une application, vous déterminez le degré d’authentification à effectuer lorsque les clients appellent l’application. Les niveaux d’authentification plus élevés fournissent une sécurité et une intégrité des données accrues, bien qu’ils entraînent généralement une dégradation des performances. Pour plus d’informations, consultez [authentification du client](client-authentication.md).

**Pour sélectionner un niveau d’authentification pour une application serveur**

1.  Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous configurez l’authentification, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .

3.  Dans la zone **niveau d’authentification pour les appels** , sélectionnez le niveau approprié. Les niveaux sont les suivants, triés de la sécurité la plus faible à la plus élevée :

    -   **Aucun**. Aucune authentification n’est effectuée.
    -   **Connectez-vous**. Authentifie les informations d'identification uniquement lorsque la connexion est établie.
    -   **Appelez**. Authentifie les informations d'identification au début de chaque appel.
    -   **Paquet**. Authentifie les informations d'identification et vérifie que toutes les données d'appel sont reçues. Il s’agit du paramètre par défaut pour les applications serveur COM+.
    -   **Intégrité des paquets**. Authentifie les informations d'identification et vérifie qu'aucune donnée d'appel n'a été modifiée lors du transit.
    -   **Confidentialité du paquet**. Authentifie les informations d'identification et chiffre le paquet, y compris les données et l'identité et la signature de l'expéditeur.

4.  Cliquez sur **OK**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



