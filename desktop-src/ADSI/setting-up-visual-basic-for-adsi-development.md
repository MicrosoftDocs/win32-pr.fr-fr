---
title: configuration de Visual Basic 6,0 pour le développement ADSI
description: cette rubrique explique comment configurer Visual Basic dans Visual Studio pour développer une application ADSI.
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- configuration de Visual Basic pour l’adsi de développement adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed2e0f4cd0b56ee0167deda2e998314bb313d1a98cd0c43a9f06b495a4324f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838679"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a>configuration de Visual Basic 6,0 pour le développement ADSI

**configuration de l’environnement de développement Microsoft Visual Studio 2010 pour Visual Basic**

1.  Démarrez Visual Studio 2010.
2.  créez un projet de Visual Basic.
3.  Ajoutez une référence à la **bibliothèque de types Active Directory**.
    > [!Note]  
    > Si vous n’avez pas besoin d’une liaison d’objet COM précoce, ignorez cette étape.

     

    1.  sélectionnez **Project \| ajouter une référence**.
    2.  Sélectionnez l’onglet **com** .
    3.  Sélectionnez **bibliothèque de types Active Directory**.

4.  Commencez à programmer avec ADSI.

avant de commencer, connectez-vous à un domaine Windows. Vous devez être autorisé à modifier la base de données Active Directory. Par défaut, l’administrateur dispose de ce privilège.

**exemple d’Application Visual Basic 6,0 : modification de FullName et Description pour un utilisateur**

1.  suivez les étapes précédentes pour créer un fichier exécutable standard Visual Basic projet.
2.  Double-cliquez sur le formulaire. Dans \_ chargement du formulaire, tapez ce qui suit. Vous devez remplacer la chaîne « LDAP : 0408 = JeffSmith, CN = Users, DC = fabrikam, DC = com » par l’ADsPath d’un utilisateur existant dans un conteneur de votre domaine. Créez un compte d’utilisateur de test qui peut être modifié à cet effet.
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  Appuyez sur **<F5>** pour exécuter le programme.
4.  Pour vérifier les modifications, utilisez l’outil de gestion utilisateurs et ordinateurs Active Directory. pour plus d’informations sur l’utilisation d’ADSI et de Visual Basic, consultez [accès à Active Directory à l’aide de Visual Basic](accessing-active-directory-using-visual-basic.md).

 

 




