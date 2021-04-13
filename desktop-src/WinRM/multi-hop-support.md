---
title: Prise en charge de plusieurs tronçons dans WinRM
description: Windows Remote Management (WinRM) prend en charge la délégation des informations d’identification de l’utilisateur sur plusieurs ordinateurs distants.
ms.assetid: 0e6c8966-bb05-4dfb-b154-300fa76e8d9c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22c3d66e8605e932fe15b812f92d51350da2d69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482808"
---
# <a name="multi-hop-support-in-winrm"></a>Prise en charge de plusieurs tronçons dans WinRM

Windows Remote Management (WinRM) prend en charge la délégation des informations d’identification de l’utilisateur sur plusieurs ordinateurs distants. La fonctionnalité de prise en charge de plusieurs tronçons peut désormais utiliser le fournisseur de services de sécurité des informations d’identification (CredSSP) pour l’authentification. CredSSP permet à une application de déléguer les informations d’identification de l’utilisateur de l’ordinateur client au serveur cible.

L’authentification CredSSP est destinée aux environnements où la délégation Kerberos ne peut pas être utilisée. La prise en charge de CredSSP a été ajoutée pour permettre à un utilisateur de se connecter à un serveur distant et d’avoir la possibilité d’accéder à un ordinateur de second saut, tel qu’un partage de fichiers.

Pour plus d’informations sur CredSSP, consultez [KB 951608](https://support.microsoft.com/kb/951608).

> [!Note]  
> Les clients et les serveurs WinRM prendront en charge l’authentification CredSSP uniquement avec des informations d’identification explicites.

 

## <a name="multi-hop-support-configuration-setup-and-details"></a>Configuration et détails de la configuration de la prise en charge de plusieurs tronçons

Il existe plusieurs mécanismes pour configurer les paramètres WinRM. Dans la procédure suivante, l’utilitaire **WinRM** et l’éditeur de stratégie de groupe (**gpedit. msc**) sont utilisés. CredSSP peut également être activé pour WinRM à l’aide de Windows PowerShell. Pour obtenir des informations de configuration détaillées et des exemples d’utilisation, consultez les applets de commande Windows PowerShell [Enable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Enable-WSManCredSSP?view=powershell-5.1&preserve-view=true), [obten-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Get-WSManCredSSP?view=powershell-5.1&preserve-view=true)et [Disable-WSManCredSSP](/powershell/module/Microsoft.WsMan.Management/Disable-WSManCredSSP?view=powershell-5.1&preserve-view=true) .

La délégation CredSSP doit être activée dans les paramètres client et dans les paramètres de service sur l’ordinateur distant. En outre, l’utilisation de CredSSP requiert la configuration d’un [*écouteur*](windows-remote-management-glossary.md) HTTP ou https sur le serveur.

**Pour configurer la prise en charge de plusieurs tronçons à l’aide de l’authentification CredSSP pour WinRM**

1.  CredSSP doit être activé dans les paramètres de configuration du client. Cet indicateur peut être activé manuellement ou par le biais d’un paramètre de stratégie de groupe. La valeur par défaut est **False**. La stratégie **autoriser l’authentification CredSSP** se trouve à l’emplacement suivant : Configuration ordinateur \\ modèle d’administration \\ composants Windows \\ Windows Remote Management (WinRM) \\ WinRM client.

    La commande suivante montre comment utiliser l’utilitaire WinRM pour activer CredSSP sur le client WinRM :

    **winrm set winrm/config/client/auth @ {CredSSP = "true"}**

2.  CredSSP doit être activé dans les paramètres de configuration du service WinRM. Cet indicateur peut être activé manuellement ou par le biais d’un paramètre de stratégie de groupe. La valeur par défaut est **False**. La stratégie **autoriser l’authentification CredSSP** se trouve à l’emplacement suivant : Configuration ordinateur \\ modèle d’administration \\ composants Windows \\ Windows Remote Management (WinRM) \\ WinRM service.

    La commande suivante montre comment utiliser l’utilitaire WinRM pour activer CredSSP sur le service WinRM :

    **winrm set winrm/config/service/auth @ {CredSSP = "true"}**

3.  Le paramètre de stratégie autoriser la délégation de nouvelles informations d’identification (**AllowFreshCredentials**) doit être activé sur le client WinRM, et un nom de principal du service (SPN) avec le préfixe WSMan doit être ajouté à la stratégie. Le SPN représente l’ordinateur cible auquel les informations d’identification de l’utilisateur peuvent être déléguées. Le SPN peut être défini sur un ou plusieurs ordinateurs. Le tableau suivant contient des exemples de formats valides pour les noms de principal du service.

    

    | SPN                                       | Description                                                                         |
    |-------------------------------------------|-------------------------------------------------------------------------------------|
    | WSMAN/myComputer. myDomain. com<br/>  | Serveur WinRM s’exécutant sur myComputer.myDomain.com.<br/>                         |
    | WSMAN/ \* . mydomain.com<br/>          | Tous les serveurs WinRM s’exécutant dans myDomain.com.<br/>                               |
    | WSMAN/ \* . fabrikam.mydomain.com<br/> | Tous les serveurs WinRM s’exécutant sur sur tous les ordinateurs dans. fabrikam.myDomain.com.<br/> |

    

     

    Pour plus d’informations sur la définition des stratégies de groupe, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).

    Pour plus d’informations sur la stratégie **AllowFreshCredentials** , consultez la description de la stratégie fournie par l’éditeur de stratégie de groupe et [KB 951608](https://support.microsoft.com/kb/951608). La stratégie **AllowFreshCredentials** se trouve à l’emplacement suivant : Configuration ordinateur \\ modèles d’administration \\ délégation des \\ informations d’identification système.

4.  Un [*écouteur*](windows-remote-management-glossary.md) HTTPS ou http doit être configuré sur le serveur. L’empreinte numérique de certificat utilisée pour configurer l' *écouteur* HTTPS est également utilisée pour configurer le paramètre CertificateThumbprint sous les paramètres du service WinRM.

    La commande suivante montre comment utiliser l’utilitaire WinRM pour configurer un [*écouteur*](windows-remote-management-glossary.md)https :

    **WinRM quickconfig-transport : https**

Si l’authentification Kerberos entre le client et le serveur n’est pas possible, l’utilisateur doit configurer l’un des paramètres suivants pour la prise en charge de plusieurs sauts :

-   Pour une meilleure sécurité, l’utilisateur doit ajouter l’attribut **CertificateThumbprint** au paramètre du service WinRM. Si le service WinRM est configuré avec un attribut **CertificateThumbprint** , le service tente de localiser le certificat correspondant dans le magasin de l’ordinateur local et utilise ce certificat pour l’authentification CredSSP. Si le service WinRM utilise un certificat du magasin de l’ordinateur local pour authentifier le serveur, le compte de service réseau doit être autorisé à accéder à la clé privée du certificat.

    > [!Note]  
    > Si le paramètre de service n’est pas configuré, le serveur WinRM utilise un certificat auto-signé qui est créé en mémoire pour chiffrer les messages envoyés au client. Toutefois, ce certificat n’est pas utilisé pour l’authentification.

     

-   Si aucune authentification Kerberos ni aucune empreinte de certificat n’est disponible, l’utilisateur peut activer l’authentification NTLM. Si l’authentification NTLM est utilisée, la stratégie autoriser les nouvelles informations d’identification avec l’authentification de serveur NTLM uniquement (**AllowFreshCredentialsWhenNTLMOnly**) doit être activée et un nom principal de service avec le préfixe WSMan doit être ajouté à la stratégie. Ce paramètre est moins sécurisé que l’authentification Kerberos et les empreintes numériques des certificats, car les informations d’identification sont envoyées à un serveur non authentifié.

    Pour plus d’informations sur la stratégie **AllowFreshCredentialsWhenNTLMOnly** , consultez la description de la stratégie fournie par l’éditeur de stratégie de groupe et [KB 951608](https://support.microsoft.com/kb/951608). La stratégie **AllowFreshCredentialsWhenNTLMOnly** se trouve à l’emplacement suivant : Configuration ordinateur \\ modèles d’administration \\ délégation des \\ informations d’identification système.

## <a name="using-credssp-authentication-with-explicit-credentials"></a>Utilisation de l’authentification CredSSP avec des informations d’identification explicites

Un utilisateur peut spécifier des informations d’identification explicites sur HTTP et HTTPs. La commande suivante montre comment utiliser l’utilitaire WinRM pour effectuer une opération distante à l’aide de l’authentification CredSSP avec des informations d’identification explicites sur HTTPs :

**WinRM OPERATION-Remote : https://myMachine -Authentication : CredSSP-username : myUsername-Password : monmotdepasse**

 

