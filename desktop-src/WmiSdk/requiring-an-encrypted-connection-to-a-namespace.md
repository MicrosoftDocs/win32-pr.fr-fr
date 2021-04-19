---
description: Vous pouvez exiger que les applications et les scripts clients établissent une connexion chiffrée pour l’authentification en ajoutant le qualificateur RequiresEncryption au fichier format MOF (MOF). MOF qui crée l’espace de noms.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Exiger une connexion chiffrée à un espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518919"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a>Exiger une connexion chiffrée à un espace de noms

Vous pouvez exiger que les applications et les scripts clients établissent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier format MOF (MOF). MOF qui crée l’espace de noms.


Une connexion chiffrée à un espace de noms WMI spécifie la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C** (ou **PktPrivacy** dans un script) pour l’authentification. Le qualificateur **RequiresEncryption** fait en sorte que WMI rejette toutes les demandes de données entrantes, sauf s’il utilise explicitement l’authentification chiffrée. Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md) ou définition de l' [authentification à l’aide de C++](setting-authentication-using-c-.md).

Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut, puis compiler à nouveau le fichier MOF. **RequiresEncryption** est utilisé dans [*MOF*](gloss-m.md) avec l’instruction de préprocesseur d' [espace de noms pragma](pragma-namespace.md) .

La procédure suivante définit l’espace de noms pour exiger une connexion chiffrée.

**Pour définir le chiffrement requis**

1.  Créez un fichier format MOF (MOF) ou modifiez votre fichier MOF existant qui définit l’espace de noms.

    L’exemple de code suivant montre que l’espace de noms qui sera modifié est le *\\ MyNamespace racine* et le fichier est nommé *MyNamespace \_ Security. mof*. **RequiresEncryption** a un type de données booléen. il doit donc être défini sur **true** ou **false**.

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  Exécutez [**mofcomp.exe**](mofcomp.md) pour compiler le fichier MOF.

    **c : \\ mofcomp MyNamespace \_ Security. mof**

    En C++, utilisez les méthodes [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

WMI rejette un client qui utilise le niveau d’authentification par défaut, car DCOM négocie la sécurité au niveau requis par le processus SVCHOST dans lequel le service WMI est en cours d’exécution. Pour plus d’informations sur les hôtes de service, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md). Pour plus d’informations sur la définition des niveaux d’authentification lors de la connexion à des espaces de noms WMI, consultez [définition du niveau de sécurité de processus par défaut à l’aide de c++](setting-the-default-process-security-level-using-c-.md), définition de l' [authentification à l’aide de C++](setting-authentication-using-c-.md), ou [définition du niveau de sécurité de processus par défaut en VBScript](setting-the-default-process-security-level-using-vbscript.md).

Lors du retour de données sur une connexion de rappel asynchrone, WMI retourne un message d’accès refusé à l’ordinateur demandeur. WMI crée également une entrée de journal dans le journal des événements NT de l’ordinateur avec l’espace de noms chiffré, indiquant qu’une connexion sécurisée ne peut pas être établie au client.

À compter de Windows Vista, le fichier WbemCore. log n’existe plus. Vous pouvez consulter le journal des événements NT pour rechercher des entrées indiquant les demandes de données entrantes rejetées à des espaces de noms qui requièrent un chiffrement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[Sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



