---
description: La \_ clé HKEY classes \_ root (HKCR) contient les associations d’extension de nom de fichier et les informations d’inscription de classe com, telles que les ProgID, les CLSID et les IID. Il est principalement destiné à la compatibilité avec le registre dans Windows 16 bits.
ms.assetid: b404875f-11e1-48f2-98d2-0378a0646ed3
title: Clé de HKEY_CLASSES_ROOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7aebe0e59424eb5ff7584fe61c2c5089eb887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868165"
---
# <a name="hkey_classes_root-key"></a>\_Clé racine de classes HKEY \_

La clé **HKEY \_ classes \_ root** (**HKCR**) contient les associations d’extension de nom de fichier et les informations d’inscription de classe com, telles que les [ProgID](../com/-progid--key.md), les [CLSID](../com/clsid-key-hklm.md)et les [IID](../com/interface-key.md). Il est principalement destiné à la compatibilité avec le registre dans Windows 16 bits.

L’inscription de classe et les informations d’extension de nom de fichier sont stockées sous les clés **HKEY \_ local \_ machine** et **HKEY \_ Current \_ User** . La clé **HKEY \_ local \_ machine \\ Software \\ classes** contient des paramètres par défaut qui peuvent s’appliquer à tous les utilisateurs sur l’ordinateur local. La clé **HKEY \_ Current \_ User \\ Software \\ classes** contient des paramètres qui s’appliquent uniquement à l’utilisateur interactif. La **clé \_ \_ racine de classes HKEY** fournit une vue du Registre qui fusionne les informations de ces deux sources. **HKEY \_ La \_ racine des classes** fournit également cette vue fusionnée pour les applications conçues pour les versions antérieures de Windows.

Les paramètres spécifiques à l’utilisateur ont priorité sur les paramètres par défaut. Par exemple, le paramètre par défaut peut spécifier une application particulière pour gérer les fichiers. doc. Toutefois, un utilisateur peut remplacer ce paramètre en spécifiant une application différente dans le registre.

Les fonctions de Registre telles que [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) ou [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa) vous permettent de spécifier la clé **\_ \_ racine de classes HKEY** . Lorsque vous appelez ces fonctions à partir d’un processus en cours d’exécution dans le compte d’utilisateur interactif, le système fusionne les paramètres par défaut dans **HKEY \_ local \_ machine \\ Software \\ classes** avec les paramètres de l’utilisateur interactif dans **HKEY \_ Current \_ User \\ Software \\ classes**. Pour plus d’informations sur la façon dont ces paramètres sont fusionnés, consultez [vue fusionnée de la \_ \_ racine de la classe HKEY](merged-view-of-hkey-classes-root.md).

Pour modifier les paramètres de l’utilisateur interactif, stockez les modifications **sous \_ HKEY \_ Current \\ User \\ classes** au lieu de **HKEY \_ classes \_ root**.

Pour modifier les paramètres par défaut, stockez les modifications sous **HKEY \_ local \_ machine \\ Software \\ classes**. Si vous écrivez des clés dans une clé sous la **\_ \_ racine de classes HKEY**, le système stocke les informations sous **HKEY \_ local \_ machine \\ Software \\ classes**. Si vous écrivez des valeurs dans une clé sous la **\_ \_ racine de la classe HKEY**, et que la clé existe déjà sous les classes de logiciels de la classe **HKEY \_ Current \_ \\ \\ User**, le système stocke les informations à cet emplacement au lieu de sous **HKEY \_ local \_ machine \\ Software \\ classes**.

Les processus qui s’exécutent dans un contexte de sécurité autre que celui de l’utilisateur interactif ne doivent pas utiliser la clé **\_ \_ racine HKEY classes** avec les fonctions de registre. Au lieu de cela, ces processus peuvent ouvrir explicitement la clé de classes de logiciels de l' **\_ \_ ordinateur \\ \\ local HKEY** pour accéder aux paramètres par défaut. Pour ouvrir une clé de Registre qui fusionne le contenu de la **\_ classe de logiciels HKEY local \_ machine \\ \\** avec les paramètres d’un utilisateur spécifié, ces processus peuvent appeler la fonction [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot) . Par exemple, un thread qui [emprunte l’identité](/windows/desktop/SecAuthZ/client-impersonation) d’un client peut appeler **RegOpenUserClassesRoot** s’il doit récupérer une vue fusionnée pour le client faisant l’objet d’un emprunt d’identité. Notez que **RegOpenUserClassesRoot** échoue si le profil utilisateur de l’utilisateur spécifié n’a pas été chargé. Le système charge automatiquement le profil de l’utilisateur interactif lors de l’ouverture de session. Pour les autres utilisateurs, vous devez appeler la fonction [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) pour charger explicitement le profil de l’utilisateur.

Si une application est exécutée avec des droits d’administrateur et que le contrôle de compte d’utilisateur est désactivé, le runtime COM ignore la configuration COM par utilisateur et accède uniquement à la configuration COM par ordinateur. Les applications qui requièrent des droits d’administrateur doivent inscrire les objets COM dépendants lors de l’installation dans le magasin de configurations COM par ordinateur (**HKEY \_ local \_ machine \\ Software \\ classes**). Pour plus d’informations, consultez [AC : UAC : COM Per-User configuration](/previous-versions/bb756926(v=msdn.10)).

**Windows Server 2003 et Windows XP/2000 :** Les applications peuvent enregistrer des objets COM dépendants dans le magasin de configuration COM par ordinateur ou par utilisateur (**HKEY \_ local \_ machine \\ Software \\ classes** ou **HKEY \_ Current \_ User \\ Software \\ classes**).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\_Racine des classes HKEY \_ (référence du Registre du kit de ressources)](/previous-versions/windows/it-pro/windows-server-2003/cc739822(v=ws.10))
</dt> </dl>

 

 
