---
title: Authentification des connexions à distance
description: Windows Remote Management assure la sécurité de la communication entre les ordinateurs en prenant en charge plusieurs méthodes standard d’authentification et de chiffrement des messages.
ms.assetid: 97a13b07-ae7a-4d2f-8841-77a22c91b204
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e9aa125f2ccf5d8c224eee645a6dba1ec2fd96e
ms.sourcegitcommit: 25c6d442ab55cbf0e065398a006b1d409349fffd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2020
ms.locfileid: "104030943"
---
# <a name="authentication-for-remote-connections"></a>Authentification des connexions à distance

Windows Remote Management assure la sécurité de la communication entre les ordinateurs en prenant en charge plusieurs méthodes standard d’authentification et de chiffrement des messages.

## <a name="default-group-access"></a>Accès au groupe par défaut

Pendant l’installation, WinRM crée le groupe **local \_ \_ WinRMRemoteWMIUsers**. WinRM limite ensuite l’accès à distance à n’importe quel utilisateur qui n’est pas membre du groupe d’administration local ou du groupe **WinRMRemoteWMIUsers \_ \_** . Vous pouvez ajouter un utilisateur local, un utilisateur de domaine ou un groupe de domaines à **WinRMRemoteWMIUsers \_ \_** en tapant **net localgroup WinRMRemoteWMIUsers \_ \_ /Add <domain> \\ <username>** à l’invite de commandes. Si vous le souhaitez, vous pouvez utiliser la stratégie de groupe pour ajouter un utilisateur au groupe.

## <a name="default-authentication-settings"></a>Paramètres d’authentification par défaut

Les informations d’identification par défaut, le nom d’utilisateur et le mot de passe, sont les informations d’identification du compte d’utilisateur connecté qui exécute le script.

**Pour passer à un autre compte sur un ordinateur distant**

1.  Spécifiez les informations d’identification dans un objet [**ConnectionOptions**](connectionoptions.md) ou [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) et fournissez-les à l’appel [**CreateSession**](wsman-createsession.md) .
2.  Définissez **WSManFlagCredUserNamePassword** dans le paramètre *Flags* de l’appel [**CreateSession**](wsman-createsession.md) .

La liste suivante contient une liste de ce qui se produit lorsqu’un script ou une application s’exécute sous les informations d’identification par défaut :

-   [*Kerberos*](windows-remote-management-glossary.md) est la méthode d’authentification par défaut lorsque le client se trouve dans un domaine et que la chaîne de destination distante ne fait pas partie des éléments suivants : localhost, 127.0.0.1 ou \[ :: 1 \] .
-   [*Negotiate*](windows-remote-management-glossary.md) est la méthode par défaut lorsque le client n’est pas dans un domaine, mais que la chaîne de destination distante est l’une des suivantes : localhost, 127.0.0.1 ou \[ :: 1 \] .

Si vous fournissez des informations d’identification explicites avec un objet [**ConnectionOptions**](connectionoptions.md) , Negotiate est la méthode par défaut. L’authentification par négociation détermine si la méthode d’authentification en cours est Kerberos ou NTLM, selon que les ordinateurs se trouvent dans un domaine ou un groupe de travail. Si vous vous connectez à un ordinateur cible distant à l’aide d’un compte local, le compte doit être préfixé avec le nom de l’ordinateur. Par exemple, myComputer \\ myUsername.

Si vous spécifiez l’authentification Negotiate, Digest ou de base et que vous ne parvenez pas à fournir un objet [**ConnectionOptions**](connectionoptions.md) , vous recevrez une erreur indiquant que des informations d’identification explicites sont requises. Si le protocole HTTPs n’est pas le transport, l’ordinateur distant cible doit être configuré dans la liste des ordinateurs hôtes approuvés.

Pour plus d’informations sur les types d’authentification activés dans les paramètres de configuration par défaut, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

## <a name="basic-authentication"></a>Authentification de base

Pour établir explicitement l’authentification de [*base*](windows-remote-management-glossary.md) dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md), définissez les indicateurs **WSManFlagUseBasic** et **WSManFlagCredUserNamePassword** dans le paramètre *Flags* . L’authentification de base est désactivée dans les paramètres de configuration par défaut pour le client WinRM et le serveur WinRM.

## <a name="digest-authentication"></a>Authentification Digest

Pour établir explicitement l’authentification [*Digest*](windows-remote-management-glossary.md) dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md), définissez l’indicateur **WSManFlagUseDigest** dans le paramètre *Flags* . Digest n’est pas pris en charge. Elle ne peut pas être configurée pour le composant serveur WinRM.

## <a name="negotiate-authentication"></a>Négocier l’authentification

Pour établir explicitement l’authentification par [*négociation*](windows-remote-management-glossary.md) , également appelée authentification intégrée de Windows, dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md), définissez l’indicateur **WSManFlagUseNegotiate** dans le paramètre *Flags* .

Le [contrôle de compte d’utilisateur (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affecte l’accès au service WinRM. Lorsque l’authentification Negotiate est utilisée dans un groupe de travail, seul le compte administrateur intégré peut accéder au service. Pour autoriser tous les comptes du groupe administrateurs à accéder au service, définissez la valeur de Registre suivante :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy** = 1

## <a name="kerberos-authentication"></a>Authentification Kerberos

Pour établir explicitement l’authentification [*Kerberos*](windows-remote-management-glossary.md) dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md), définissez l’indicateur **WSManFlagUseKerberos** dans le paramètre *Flags* . Le client et le serveur doivent tous les deux être joints à un domaine. Si vous utilisez Kerberos comme méthode d’authentification, vous ne pouvez pas utiliser une adresse IP dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession).

## <a name="client-certificate-based-authentication"></a>Authentification par certificat client

Pour établir l’authentification par certificat client dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md), définissez l’indicateur **WSManFlagUseClientCertificate** dans le paramètre *Flags* .

Vous devez d’abord activer l’authentification par certificat à la fois sur le client et le service à l’aide de l’outil en ligne de commande WinRM. Pour plus d’informations, consultez [activation des options d’authentification](#enabling-or-disabling-authentication-options). Vous devez également créer une entrée dans la table CertMapping sur l’ordinateur serveur WinRM. Cela établit un mappage entre un ou plusieurs certificats et un compte local. Une fois le certificat utilisé pour l’authentification et l’autorisation, le compte local correspondant est utilisé pour les opérations effectuées par le service WinRM.

Le mappage peut être créé pour un URI de ressource spécifique. Pour plus d’informations, notamment sur la création d’une entrée de table CertMapping, tapez **WinRM Help CertMapping** à l’invite de commandes.

> [!Note]  
> La taille maximale du certificat utilisable par WinRM dans ce contexte est de 16 Ko.

 

## <a name="enabling-or-disabling-authentication-options"></a>Activation ou désactivation des options d’authentification

L’option d’authentification par défaut lors de l’installation du système est Kerberos. Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

Si votre script ou votre application requiert une méthode d’authentification spécifique qui n’est pas activée, vous devez modifier la configuration pour activer ce type d’authentification. Cette modification peut être effectuée à l’aide de l’outil de ligne de commande **WinRM** ou de stratégie de groupe pour l' **objet Windows Remote Management stratégie de groupe**. Vous pouvez également choisir de désactiver certaines méthodes d’authentification.

**Pour activer ou désactiver l’authentification avec l’outil WinRM**

1.  Pour définir la configuration du client WinRM, utilisez la commande **winrm set** et spécifiez le client. Par exemple, la commande suivante désactive l’authentification Digest pour le client.

    **winrm set winrm/config/client/auth @ {Digest = "false"}**

2.  Pour définir la configuration du serveur WinRM, utilisez la commande **winrm set** et spécifiez le service. Par exemple, la commande suivante active l’authentification Kerberos pour le service.

    **winrm set winrm/config/service/auth @ {Kerberos = "true"}**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> </dl>

 

 




