---
title: Configuration de Visual C++ 6,0 pour le développement ADSI
description: Cette rubrique vous montre comment configurer C++ dans Visual Studio afin de pouvoir développer une application ADSI.
ms.assetid: 6f1ab3eb-2e0b-4f3e-b93c-e24c8b3b1a27
ms.tgt_platform: multiple
keywords:
- Configuration de C++ pour le développement ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f2350b88402c921d014b0c93756759a1d0f744
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028550"
---
# <a name="setting-up-visual-c-60-for-adsi-development"></a>Configuration de Visual C++ 6,0 pour le développement ADSI

Le système de développement Microsoft Visual C++ 6,0 peut être utilisé pour développer des applications d’entreprise. Pour configurer votre environnement Visual C++ 6,0 pour développer une application ADSI, procédez comme suit :

**Configuration de l’environnement de développement Microsoft Visual C++ 6,0**

1.  Pointez sur le répertoire include et la bibliothèque. Sélectionnez **outils \| options**. Cliquez sur l’onglet **répertoire** et spécifiez le chemin d’accès aux fichiers d’en-tête ADSI.
2.  Incluez le fichier activeds. h dans votre projet.
3.  Ajoutez les fichiers activeds. lib et adsiid. lib à l’entrée de l’éditeur de liens pour votre projet.
4.  Commencez à programmer avec ADSI.

Connectez-vous à un domaine Windows. Vous devez également avoir l’autorisation de modifier les données dans Active Directory. Par défaut, l’administrateur dispose de ce privilège. Pour entrer cet exemple de code :

**Exemple d’application Visual C++ : création d’un utilisateur dans un domaine**

1.  Démarrez Visual C++ 6,0.
2.  Créez un projet exécutable autonome. Il peut s’agir d’une application MFC, ATL ou console.
3.  Suivez les étapes précédentes pour configurer votre projet.
4.  Entrez l’exemple de code suivant. Remplacez la chaîne « LDAP :As = Users, DC = fabrikam, DC = com » par le chemin ADsPath d’un conteneur dans votre domaine. Vous devez également remplacer le nom d’utilisateur « JeffSmith » par un nom d’utilisateur unique dans votre domaine.

    ```C++
    #include "stdafx.h"
    #include "activeds.h"

    int main(int argc, char* argv[])
    {
        HRESULT hr;
        IADsContainer *pCont;
        IDispatch *pDisp=NULL;
        IADs *pUser;

         // Initialize COM before calling any ADSI functions or interfaces.
         CoInitialize(NULL);

        hr = ADsGetObject( L"LDAP://CN=users,DC=fabrikam,DC=com", 
                                   IID_IADsContainer, 
                                   (void**) &pCont );
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        //-----------------
        // Create a user
        //-----------------
        
        hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=jeffsmith"), &pDisp );
        
        // Release the container object.    
        pCont->Release();
        
        if ( !SUCCEEDED(hr) )
        {
            return 0;
        }

        hr = pDisp->QueryInterface( IID_IADs, (void**) &pUser );

        // Release the dispatch interface.
        pDisp->Release();

        if ( !SUCCEEDED(hr) )
        {    
            return 0;
        }

        // Commit the object data to the directory.
        pUser->SetInfo();

        // Release the object.
        pUser->Release();

        CoUninitialize();
    }
    ```

    

5.  Générez et exécutez l’application. Pour vérifier que l’utilisateur a été créé, utilisez l’outil de gestion utilisateurs et ordinateurs Active Directory.

 

 




