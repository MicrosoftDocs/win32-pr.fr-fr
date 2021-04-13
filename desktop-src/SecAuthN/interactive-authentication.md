---
description: L’authentification est interactive quand un utilisateur est invité à fournir des informations d’ouverture de session. L’autorité de sécurité locale (LSA) effectue une authentification interactive lorsqu’un utilisateur se connecte par le biais de l’interface utilisateur GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Authentification interactive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320201"
---
# <a name="interactive-authentication"></a><span data-ttu-id="f7cc4-104">Authentification interactive</span><span class="sxs-lookup"><span data-stu-id="f7cc4-104">Interactive Authentication</span></span>

<span data-ttu-id="f7cc4-105">L’authentification est interactive quand un utilisateur est invité à fournir des informations d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-105">Authentication is interactive when a user is prompted to supply logon information.</span></span> <span data-ttu-id="f7cc4-106">L' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) effectue une authentification interactive lorsqu’un utilisateur se connecte par le biais de l’interface utilisateur [*Gina*](../secgloss/g-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f7cc4-106">The [*Local Security Authority*](../secgloss/l-gly.md) (LSA) performs an interactive authentication when a user logs on through the [*GINA*](../secgloss/g-gly.md) user interface.</span></span> <span data-ttu-id="f7cc4-107">L’illustration suivante montre les parties d’une authentification interactive classique.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-107">The following illustration shows the parts of a typical interactive authentication.</span></span>

![authentification interactive](images/lsaint3.png)

<span data-ttu-id="f7cc4-109">Un utilisateur signale au système de commencer la séquence d’ouverture de session en tapant la [*séquence*](../secgloss/s-gly.md) de touches Ctrl + Alt + Suppr (SAS).</span><span class="sxs-lookup"><span data-stu-id="f7cc4-109">A user signals the system to begin the logon sequence by typing the CTRL+ALT+DEL [*secure attention sequence*](../secgloss/s-gly.md) (SAS).</span></span> <span data-ttu-id="f7cc4-110">[*Winlogon*](../secgloss/w-gly.md) reçoit la SAP et appelle Gina pour afficher une interface utilisateur et obtenir les données d’ouverture de session de l’utilisateur, telles qu’un nom d’utilisateur et un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-110">[*Winlogon*](../secgloss/w-gly.md) receives the SAS and calls the GINA to display a user interface and obtain the user's logon data, such as a user name and password.</span></span>

<span data-ttu-id="f7cc4-111">Après avoir obtenu les données de connexion, GINA appelle la fonction [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) pour authentifier l’utilisateur, en spécifiant le package d’authentification qui doit être utilisé pour évaluer les données d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-111">After obtaining the logon data, the GINA calls the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) function to authenticate the user, specifying which authentication package must be used to evaluate the logon data.</span></span>

<span data-ttu-id="f7cc4-112">L’autorité LSA appelle le package d’authentification spécifié et lui transmet les données de connexion.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-112">The LSA calls the specified authentication package and passes the logon data to it.</span></span> <span data-ttu-id="f7cc4-113">Le package d’authentification examine les données et détermine si l’authentification réussit.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-113">The authentication package examines the data and determines whether the authentication is successful.</span></span> <span data-ttu-id="f7cc4-114">Le résultat de l’authentification est retourné à l’autorité LSA et du LSA au GINA.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-114">The authentication result is returned to the LSA and from the LSA, to the GINA.</span></span>

<span data-ttu-id="f7cc4-115">GINA affiche la réussite ou l’échec de l’authentification de l’utilisateur et renvoie le résultat de l’authentification à Winlogon.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-115">The GINA displays the success or failure of the authentication to the user and returns the result of the authentication to Winlogon.</span></span> <span data-ttu-id="f7cc4-116">Si l’authentification a échoué, la session d’ouverture de session de l’utilisateur commence et un ensemble d' [*informations d’identification*](../secgloss/c-gly.md) de connexion sont enregistrées pour référence ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-116">If the authentication succeeds, the user's logon session begins and a set of logon [*credentials*](../secgloss/c-gly.md) are saved for future reference.</span></span>

> [!Note]  
> <span data-ttu-id="f7cc4-117">En général, un développeur qui écrit une GINA personnalisée pour accepter des données de connexion spécialisées, telles qu’une [*carte à puce*](../secgloss/s-gly.md) ou des données d’analyse rétinienne, doit également écrire un package d’authentification responsable du traitement de ces données et de la détermination de son authenticité.</span><span class="sxs-lookup"><span data-stu-id="f7cc4-117">In general, a developer who writes a custom GINA to accept specialized logon data, such as a [*smart card*](../secgloss/s-gly.md) or retinal-scan data, must also write an authentication package responsible for processing that data and determining its authenticity.</span></span>

 

<span data-ttu-id="f7cc4-118">Pour plus d’informations sur Winlogon et les GINA, consultez [Winlogon et Gina](winlogon-and-gina.md).</span><span class="sxs-lookup"><span data-stu-id="f7cc4-118">For more information about Winlogon and GINAs, see [Winlogon and GINA](winlogon-and-gina.md).</span></span> <span data-ttu-id="f7cc4-119">Pour plus d’informations sur les packages d’authentification, consultez [création de packages de sécurité personnalisés](creating-custom-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="f7cc4-119">For more information about authentication packages, see [Creating Custom Security Packages](creating-custom-security-packages.md).</span></span>

 

 
