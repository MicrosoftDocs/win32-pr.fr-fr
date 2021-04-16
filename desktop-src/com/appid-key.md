---
title: Clé AppID
description: Regroupe les options de configuration pour un ou plusieurs objets DCOM dans un emplacement centralisé dans le registre. Les objets DCOM hébergés par le même exécutable sont regroupés en un seul AppID pour simplifier la gestion des paramètres de configuration et de sécurité courants.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- Clé de Registre AppID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383003"
---
# <a name="appid-key"></a>Clé AppID

Regroupe les options de configuration pour un ou plusieurs objets DCOM dans un emplacement centralisé dans le registre. Les objets DCOM hébergés par le même exécutable sont regroupés en un seul AppID pour simplifier la gestion des paramètres de configuration et de sécurité courants.

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ Classes de logiciels de l' \_ ordinateur local \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Valeur de Registre                                           | Description                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | Décrit la liste de Access Control (ACL) des principaux qui peuvent accéder aux instances de cette classe. Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). |
| [**ActivateAtStorage**](activateatstorage.md)           | Configure le client pour instancier des objets sur le même ordinateur que l’état persistant qu’ils utilisent ou à partir desquels ils sont initialisés.                                                                    |
| [**AppID**](appid.md)                                   | Identifie le GUID AppID qui correspond à l’exécutable nommé.                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | Configure la façon dont un serveur COM configuré pour s’exécuter en tant qu’utilisateur interactif est lancé ou lié par un client dans un bureau autre que celui par défaut.                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Définit le niveau d’authentification pour les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou pour les applications qui appellent **CoInitializeSecurity** et spécifient un AppID.               |
| [**DllSurrogate**](dllsurrogate.md)                     | Permet aux serveurs DLL de s’exécuter dans un processus de substitution. Si une chaîne vide est spécifiée, le substitut fourni par le système est utilisé ; Sinon, la valeur spécifie le chemin d’accès du substitut à utiliser.                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre [**DllSurrogate**](dllsurrogate.md) .                                                                          |
| [**Points de terminaison**](endpoints.md)                           | Configure une application COM pour utiliser un numéro de port TCP spécifié pour les communications DCOM.                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | Décrit la liste de Access Control (ACL) des principaux qui peuvent démarrer de nouveaux serveurs pour cette classe.                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | Détermine si COM doit charger le profil utilisateur pour les serveurs COM qui exécutent en tant qu’identité de l’application utilisateur de lancement.                                                                                           |
| [**LocalService**](localservice.md)                     | Installe un objet en tant qu’application de service.                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | Définit l’architecture préférée, 32 bits ou 64 bits, pour ce serveur COM.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Configure le client de façon à ce qu’il demande à l’objet d’être exécuté sur un ordinateur particulier chaque fois qu’une fonction d’activation est appelée pour laquelle aucune structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) n’est spécifiée.              |
| [**ROTFlags**](rotflags.md)                             | Contrôle l’inscription d’un serveur COM dans la table ROT (Running Object Table).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Configure une classe pour qu’elle s’exécute sous un compte d’utilisateur spécifique lorsqu’elle est activée par un client distant sans être écrite comme une application de service.                                                                       |
| [**ServiceParameters**](serviceparameters.md)           | Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre [**LocalService**](localservice.md) .                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Définit le niveau de confiance de la stratégie de restriction logicielle (SRP) pour les applications.                                                                                                                                        |



 

## <a name="remarks"></a>Notes

Les AppID sont mappés à des exécutables et à des classes à l’aide de deux mécanismes différents :

-   À l’aide d’un identificateur global unique (GUID) 128 bits qui identifie la clé **AppID** . Une classe indique son AppID correspondant sous la clé [**CLSID**](clsid-key-hklm.md) dans une valeur nommée « AppID ». Ce mappage est utilisé lors de l’activation.
-   Utilisation d’une valeur nommée qui indique un nom d’exécutable (par exemple, « MYOLDAPP.EXE »). Cette valeur nommée est de type **reg \_ SZ** et contient la représentation sous forme de chaîne de l’AppID associé à l’exécutable. Ce mappage est utilisé pour obtenir les autorisations d’accès et le niveau d’authentification par défaut.

La clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** correspond à la clé **\_ \_ racine HKEY classes** , qui a été conservée pour la compatibilité avec les versions antérieures de com.

Pour les serveurs COM, le mappage est généralement généré et écrit dans le registre pendant le processus d’inscription ou lors de l’exécution de dcomcnfg.exe. Toutefois, les clients COM qui souhaitent définir la sécurité à l’aide de la clé **AppID** doivent créer les clés de Registre appropriées et spécifier le mappage requis en appelant les [fonctions du registre](/windows/desktop/SysInfo/registry-functions) ou en utilisant Regedit.exe. Des valeurs telles que [**AccessPermission**](accesspermission.md) ou [**AuthenticationLevel**](authenticationlevel.md) peuvent être définies pour le client. Par exemple, supposons que le nom de votre exécutable pour votre processus client est « YourClient.exe » et que vous souhaitez définir le niveau d’authentification sur « aucun ». Vous pouvez utiliser Guidgen.exe ou Uuidgen.exe pour créer le GUID qui est l’AppID pour votre exécutable. Vous devez ensuite définir des valeurs dans le registre, comme indiqué dans l’exemple suivant, où 00000001 représente un niveau d’authentification « None » :

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 