---
description: Si vous utilisez l’API de script pour WMI, vous pouvez définir des privilèges de sécurité spécifiques.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Exécution d’opérations privilégiées à l’aide de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eaf235bd1c9a5b0febb88d7ed587bfdf63f52c74cf5027273e447d7f3fb5cdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108954"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Exécution d’opérations privilégiées à l’aide de VBScript

Si vous utilisez l’API de script pour WMI, vous pouvez définir des privilèges de sécurité spécifiques. Par exemple, vous pouvez définir les privilèges de sécurité pour demander un arrêt du système d’exploitation ou pour examiner le journal des événements de sécurité. Pour plus d’informations, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

Vous devez uniquement définir des privilèges lorsque vous accédez à WMI sur votre ordinateur. Lorsque vous accédez à un hôte distant, COM RPC définit automatiquement les privilèges. Pour déterminer tous les privilèges requis, consultez la documentation relative aux classes WMI spécifiques auxquelles vous souhaitez accéder, telles que [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem). Pour plus d’informations, consultez [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

Les sections suivantes sont présentées dans cette rubrique :

-   [Définition d’un privilège à partir de l’objet de sécurité \_](/windows)
-   [Définition d’un privilège dans le cadre d’un moniker](#setting-a-privilege-as-part-of-a-moniker)
-   [Révocation et réinitialisation des privilèges](#revoking-and-resetting-privileges)
-   [Rubriques connexes](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Définition d’un privilège à partir de l’objet de sécurité \_

Utilisez la procédure suivante pour définir des privilèges de sécurité dans Visual Basic.

**Pour définir des privilèges dans Visual Basic**

1.  Créez un objet de type [**SWbemLocator**](swbemlocator.md).
2.  Ajoutez le nouveau privilège à l’objet [**SWbemLocator. \_ Security**](swbemlocator-security-.md) .

    L’objet de [**sécurité \_**](swbemlocator-security-.md) contient une collection [**SWbemObjectSet**](swbemobjectset.md) . Les objets du jeu sont des objets [**SWbemSecurity**](swbemsecurity.md) . Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).

3.  Connectez-vous à WMI et récupérez un objet [**SWbemServices**](swbemservices.md) .

    L’objet [**SWbemServices**](swbemservices.md) hérite du privilège défini à l’étape précédente.

Vous pouvez également définir un privilège à l’aide de la méthode [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Définition d’un privilège dans le cadre d’un moniker

Vous pouvez définir un privilège dans le cadre d’un moniker.

L’exemple suivant montre comment ajouter un privilège de débogage à un moniker.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Révocation et réinitialisation des privilèges

L’exemple suivant montre comment définir le privilège **SeDebugPrivilege** et révoquer le privilège **SeRemoteShutdownPrivilege** .


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> </dl>

 

 
