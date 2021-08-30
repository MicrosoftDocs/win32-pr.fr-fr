---
title: Désactivation de la sécurité d’activation
description: Désactivation de la sécurité d’activation
ms.assetid: 3474f8ad-f041-4886-ad39-ff0603c5c69e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3510f32b616db1a8394fa5b91cce6ae22becd797b330fc981d3d3f73d6e614cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992099"
---
# <a name="turning-off-activation-security"></a>Désactivation de la sécurité d’activation

Normalement, l’activation utilise des paramètres de sécurité par défaut. Toutefois, vous pouvez contrôler la sécurité d’activation en spécifiant une structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) , qui est un membre de la structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) qui est passée aux fonctions d’activation. Si le client spécifie un niveau d’authentification RPC \_ C \_ Authn \_ niveau \_ None dans la structure **COAUTHINFO** , l’authentification n’est pas tentée. Dans le cas contraire, une tentative d’activation sécurisée est tentée et, si l’authentification échoue, l’activation échoue.

Si le client ne spécifie pas une structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) explicite et définit plutôt le pointeur sur **null**, com tente d’authentifier le client. S’il ne peut pas authentifier le client, COM vérifie le descripteur de sécurité d’autorisation d’exécution pour déterminer s’il existe une liste DACL **null** ou une liste de contrôle d’accès qui autorise l’accès à tout le monde. Si cette vérification s’effectue correctement, le serveur est lancé. Par conséquent, même si le client ne spécifie pas de structure **COAUTHINFO**, une activation non sécurisée peut avoir lieu lorsque le serveur le permet.

> [!Note]  
> Pour permettre aux utilisateurs réseau non authentifiés d’exécuter une application COM, les rôles d’application doivent inclure l’utilisateur anonyme. à compter de Windows Server 2003, par défaut, l’utilisateur anonyme n’est pas inclus dans le groupe tout le monde.

 

Pourquoi un client souhaite-t-il désactiver la sécurité d’activation de manière explicite même si l’activation non sécurisée finira par se produire si le serveur l’autorise ? Étant donné que la désactivation explicite de la sécurité d’activation augmente les performances lorsque le client ne souhaite pas ou n’a pas besoin de vérifications de sécurité.

Les opérations suivantes doivent être effectuées pour désactiver explicitement la sécurité d’activation :

-   Le client doit spécifier un niveau d’authentification du \_ \_ niveau AUTHn RPC- \_ \_ None dans la structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) qui est membre de la structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fournie à la fonction d’activation.
-   Le client doit spécifier un niveau d’emprunt d’identité de l' \_ emprunt d’identité RPC C \_ IMP \_ \_ dans la structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) qui est membre de la structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) fournie à la fonction d’activation. Si cette valeur n’est pas passée, le serveur RPC \_ S Server n’est pas \_ \_ disponible.
-   Le serveur doit spécifier **tout le monde** pour les **autorisations de lancement par défaut**. La méthode recommandée pour effectuer cette tâche consiste à utiliser Dcomcnfg.exe comme suit :
    1.  Exécutez Dcomcnfg.exe.
    2.  Dans la page **applications** , sélectionnez l’application qui représente le serveur. Cliquez sur le bouton des **Propriétés** (ou double-cliquez sur l’application sélectionnée).
    3.  Sur la page de propriétés **sécurité** , cliquez sur le bouton **utiliser des autorisations d’exécution personnalisées** .
    4.  Cliquez sur le bouton **modifier** dans la zone **autorisations d’exécution** .
    5.  Dans la boîte de dialogue autorisations de la **valeur du Registre** , cliquez sur le bouton **Ajouter** .
    6.  Sélectionnez l’entrée pour **tout le monde** dans la zone de liste.
    7.  Dans la zone **de liste type d’accès** , choisissez **autoriser le lancement**.
    8.  Cliquez sur le bouton **OK** .

> [!Note]  
> dans Windows Server 2003, la fonctionnalité d’authentification de l’application système COM+ comprend la valeur EOAC \_ DISABLE \_ AAA. Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système. La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désactivation de la sécurité de l’appel](turning-off-call-security.md)
</dt> </dl>

 

 