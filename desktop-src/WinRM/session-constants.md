---
title: Constantes de session
description: Les constantes de session dans l' \_ \_ énumération WSManSessionFlags spécifient l’authentification et d’autres informations pour les appels WSMan. CreateSession ou IWSMan CreateSession qui se connectent à un ordinateur distant.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106533536"
---
# <a name="session-constants"></a><span data-ttu-id="c164e-103">Constantes de session</span><span class="sxs-lookup"><span data-stu-id="c164e-103">Session Constants</span></span>

<span data-ttu-id="c164e-104">Les constantes de session dans l’énumération **\_ \_ WSManSessionFlags** spécifient l’authentification et d’autres informations pour les appels [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) qui se connectent à un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="c164e-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="c164e-105">Ces constantes sont également étroitement liées aux commutateurs de l’outil en ligne de commande **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="c164e-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="c164e-106">Utilisation de constantes de session</span><span class="sxs-lookup"><span data-stu-id="c164e-106">Using Session Constants</span></span>

<span data-ttu-id="c164e-107">Vous pouvez définir les indicateurs de session pour l’appel à [**WSMan. CreateSession**](wsman-createsession.md) de deux façons différentes.</span><span class="sxs-lookup"><span data-stu-id="c164e-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="c164e-108">L’un est plus rapide et plus simple.</span><span class="sxs-lookup"><span data-stu-id="c164e-108">One is shorter and simpler.</span></span> <span data-ttu-id="c164e-109">La méthode la plus longue, comme indiqué dans l’exemple suivant, consiste à localiser la valeur de l’indicateur que vous souhaitez utiliser et à créer dans votre script une constante avec cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c164e-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="c164e-110">La constante est ensuite utilisée pour définir la valeur du paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="c164e-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="c164e-111">La méthode recommandée, comme indiqué dans l’exemple suivant, consiste à utiliser la méthode d’objet [**WSMan**](wsman.md) associée à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="c164e-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="c164e-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes d’authentification**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c164e-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="c164e-113">Spécifiez la méthode d’authentification et la manière de gérer les serveurs de certificats.</span><span class="sxs-lookup"><span data-stu-id="c164e-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="c164e-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Autres constantes de session**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="c164e-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="c164e-115">Spécifiez l’encodage, le chiffrement et le port du nom de principal du service.</span><span class="sxs-lookup"><span data-stu-id="c164e-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="c164e-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c164e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c164e-117">Constantes et énumérations WinRM</span><span class="sxs-lookup"><span data-stu-id="c164e-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="c164e-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="c164e-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="c164e-119">Authentification des connexions à distance</span><span class="sxs-lookup"><span data-stu-id="c164e-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




