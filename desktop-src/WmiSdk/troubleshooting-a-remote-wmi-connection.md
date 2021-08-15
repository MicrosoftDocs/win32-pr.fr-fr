---
description: Les sections suivantes décrivent les problèmes courants que les développeurs peuvent rencontrer avec la création d’une connexion WMI à distance.
ms.assetid: 328e420b-a859-4ce9-8a31-67150eb0a78f
ms.tgt_platform: multiple
title: Résolution des problèmes d’une connexion WMI à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10603f713fecf861750d70c4166da91e081dc273a0d6d6134ed916a7f84f2bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312415"
---
# <a name="troubleshooting-a-remote-wmi-connection"></a>Résolution des problèmes d’une connexion WMI à distance

Les sections suivantes décrivent les problèmes courants que les développeurs peuvent rencontrer avec la création d’une connexion WMI à distance.

Les sections suivantes sont présentées dans cette rubrique :

-   [Accès DCOM refusé](#dcom-access-denied)
-   [Échec de la Connecter](#failure-to-connect)
-   [Expiration de la connexion WMI](#wmi-connection-timed-out)
-   [Rubriques connexes](#related-topics)

## <a name="dcom-access-denied"></a>Accès DCOM refusé

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice
</dt> <dd>

votre connexion a échoué avec l’erreur « accès DCOM refusé », ainsi que la valeur décimale-2147024891 ou Hex value0x80070005.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique
</dt> <dd>

DCOM n’est peut-être pas configuré pour autoriser une connexion WMI.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768
</dt> <dd>

Vous pouvez configurer les paramètres DCOM pour WMI à l’aide de l’utilitaire de configuration DCOM (**DCOMCnfg.exe**) disponible dans **Outils d’administration** dans le **panneau** de configuration. Cet utilitaire expose les paramètres qui permettent à certains utilisateurs de se connecter à l’ordinateur à distance via DCOM. Les membres du groupe administrateurs sont autorisés à se connecter à distance à l’ordinateur par défaut. Avec cet utilitaire, vous pouvez définir la sécurité pour démarrer, accéder et configurer le service WMI.

Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).

</dd> </dl>

## <a name="failure-to-connect"></a>Échec de la Connecter

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice
</dt> <dd>

Vous ne pouvez pas vous connecter à WMI sur un système distant.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique
</dt> <dd>

Vous essayez peut-être de vous connecter à un système qui ne prend pas en charge WMI. Les connexions suivantes entre les versions de système d’exploitation ne sont pas prises en charge :

-   Vous ne pouvez pas vous connecter à un ordinateur qui exécute une édition Starter, de base ou personnelle.

Vous pouvez également essayer de vous connecter à un espace de noms qui nécessite une connexion chiffrée, qui requiert un niveau d’authentification `pktPrivacy` , **WbemAuthenticationLevelPktPrivacy** ou une déclaration de **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768
</dt> <dd>

Pour plus d’informations, consultez [sécurisation des espaces de noms WMI](securing-wmi-namespaces.md), [sécurisation des clients et fournisseurs C++](securing-c---clients-and-providers.md), ou [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

</dd> </dl>

## <a name="wmi-connection-timed-out"></a>Expiration de la connexion WMI

<dl> <dt>

<span id="Symptom"></span><span id="symptom"></span><span id="SYMPTOM"></span>Indice
</dt> <dd>

Votre connexion WMI expire.

</dd> <dt>

<span id="Issue"></span><span id="issue"></span><span id="ISSUE"></span>Problématique
</dt> <dd>

En raison de problèmes de latence du réseau, l’ordinateur ne peut tout simplement pas répondre dans le temps.

</dd> <dt>

<span id="Resolution"></span><span id="resolution"></span><span id="RESOLUTION"></span>768
</dt> <dd>

Lors de la connexion à WMI via un appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), vous pouvez définir l’indicateur **wbemConnectFlagUseMaxWait** (script) ou la valeur de l' **\_ indicateur WBEM \_ Connect \_ use \_ Max \_ Wait** en C++ sur 128 (0x80) pour imposer un délai de deux (2) minutes sur l’appel.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 



