---
title: Détermination de vos besoins en matière de sécurité
description: La façon dont vous configurez la sécurité COM pour votre application dépend du type de sécurité dont votre application a besoin. Il existe plusieurs situations courantes qui déterminent ce que vous devez faire.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cacef6d4e3aab59cb3b603125c36dd17d07846
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675822"
---
# <a name="determining-your-security-needs"></a><span data-ttu-id="f1181-104">Détermination de vos besoins en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="f1181-104">Determining Your Security Needs</span></span>

<span data-ttu-id="f1181-105">La façon dont vous configurez la sécurité COM pour votre application dépend du type de sécurité dont votre application a besoin.</span><span class="sxs-lookup"><span data-stu-id="f1181-105">How you set up COM security for your application depends on what kind of security your application needs.</span></span> <span data-ttu-id="f1181-106">Il existe plusieurs situations courantes qui déterminent ce que vous devez faire.</span><span class="sxs-lookup"><span data-stu-id="f1181-106">There are several common situations that determine what you should do.</span></span>

<span data-ttu-id="f1181-107">Si vous décidez d’utiliser les valeurs par défaut de sécurité COM, vous n’avez pas à faire anythingâ. COM les gère tous.</span><span class="sxs-lookup"><span data-stu-id="f1181-107">If you decide to use the COM security defaults, you do not have to do anythingâ€”COM handles it all.</span></span> <span data-ttu-id="f1181-108">Pour plus d’informations sur ce que sont ces paramètres par défaut, consultez [valeurs par défaut de la sécurité com](com-security-defaults.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-108">For information on what these default settings are, see [COM Security Defaults](com-security-defaults.md).</span></span>

<span data-ttu-id="f1181-109">Vous pouvez également empêcher tout appel distant sur votre ordinateur en désactivant DCOM (COM entre les ordinateurs distants).</span><span class="sxs-lookup"><span data-stu-id="f1181-109">You can also prevent any remote calls into your machine by disabling DCOM altogether (COM between remote computers).</span></span> <span data-ttu-id="f1181-110">Pour plus d’informations, consultez Définition de la [sécurité System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-110">For more information, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="f1181-111">Pour les applications héritées ou nouvelles, vous pouvez définir la sécurité au niveau du processus dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f1181-111">For legacy or new applications, you can set process-wide security in the registry.</span></span> <span data-ttu-id="f1181-112">Pour plus d’informations, consultez [définition de la sécurité échelle dans le registre](setting-processwide-security-through-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-112">For more information, see [Setting Processwide Security Through the Registry](setting-processwide-security-through-the-registry.md).</span></span>

<span data-ttu-id="f1181-113">Vous pouvez également remplacer les paramètres de sécurité par défaut pour les appels à certaines interfaces dans le processus lors de la définition de la sécurité par défaut pour le reste du processus (pour permettre à COM de gérer les cas généraux).</span><span class="sxs-lookup"><span data-stu-id="f1181-113">You can also override default security settings for calls to certain interfaces in the process while setting default security for the remainder of the process (to allow COM to handle the general cases).</span></span> <span data-ttu-id="f1181-114">Pour plus d’informations, consultez [définition de la sécurité au niveau du proxy de l’interface](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-114">For more information, see [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="f1181-115">Pour les exigences de sécurité complexes, vous pouvez gérer l’ensemble de la sécurité par programmation plutôt que de permettre à COM de la gérer à votre place.</span><span class="sxs-lookup"><span data-stu-id="f1181-115">For complex security requirements, you can handle all security programmatically rather than allowing COM to handle it for you.</span></span> <span data-ttu-id="f1181-116">Pour ce faire, appelez [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) pour désactiver l’authentification automatique, puis Contrôlez tous les paramètres de sécurité en définissant la sécurité sur une base de proxy par interface.</span><span class="sxs-lookup"><span data-stu-id="f1181-116">To do this, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) to disable automatic authentication, and then control all the security settings by setting security on a per-interface proxy basis.</span></span> <span data-ttu-id="f1181-117">Pour plus d’informations, consultez Définition de la [sécurité échelle avec CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) et [définition de la sécurité au niveau du proxy d’interface](setting-security-at-the-interface-proxy-level.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-117">For more information, see [Setting Processwide Security with CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) and [Setting Security at the Interface Proxy Level](setting-security-at-the-interface-proxy-level.md).</span></span>

<span data-ttu-id="f1181-118">Dans certains scénarios, vous souhaiterez peut-être désactiver complètement la sécurité.</span><span class="sxs-lookup"><span data-stu-id="f1181-118">In some scenarios, you might want to turn off security completely.</span></span> <span data-ttu-id="f1181-119">Vous pouvez décider que votre application n’a pas besoin de sécurité, ou vous souhaiterez peut-être désactiver la sécurité pendant le développement afin que vous puissiez activer les fonctionnalités de sécurité individuellement.</span><span class="sxs-lookup"><span data-stu-id="f1181-119">You might decide that your application does not need any security, or you might want to disable security during development time so that you can enable security features individually.</span></span> <span data-ttu-id="f1181-120">Pour savoir comment désactiver la sécurité COM, consultez Désactivation de la [sécurité](turning-off-security.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-120">To learn how to disable COM security, see [Turning Off Security](turning-off-security.md).</span></span>

<span data-ttu-id="f1181-121">La sécurité dans COM s’appuie sur les services d’authentification administrés par les packages de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f1181-121">Security in COM relies on authentication services administered by security packages.</span></span> <span data-ttu-id="f1181-122">NTLMSSP fonctionne bien pour de nombreuses applications, mais il ne fournit pas la sécurité la plus robuste offerte par d’autres packages.</span><span class="sxs-lookup"><span data-stu-id="f1181-122">NTLMSSP works well for many applications but does not provide the more robust security offered by other packages.</span></span> <span data-ttu-id="f1181-123">Par conséquent, COM prend en charge le package de sécurité Schannel et le protocole de sécurité Kerberos V5.</span><span class="sxs-lookup"><span data-stu-id="f1181-123">Therefore, COM supports the Schannel security package and the Kerberos v5 security protocol.</span></span> <span data-ttu-id="f1181-124">Pour plus d’informations sur l’utilisation de ces packages de sécurité, consultez [com et packages de sécurité](com-and-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="f1181-124">For more details on using these security packages, see [COM and Security Packages](com-and-security-packages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1181-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1181-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1181-126">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="f1181-126">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




