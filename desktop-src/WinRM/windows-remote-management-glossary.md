---
title: Glossaire Windows Remote Management
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bbda0db7-f473-444b-85ab-f3c5240c4b18
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b6d7411063fbb117c68e211181142ac773f924
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106523768"
---
# <a name="windows-remote-management-glossary"></a><span data-ttu-id="b0118-103">Glossaire Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="b0118-103">Windows Remote Management Glossary</span></span>


<dl> <dt>

<span data-ttu-id="b0118-104">WSMan : éléments \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="b0118-104">\*\*\*\*wsman:Items\*\*\*\*</span></span>
</dt> <dd>

<span data-ttu-id="b0118-105">Élément de protocole WS-Management retourné dans une énumération qui obtient à la fois les instances et l’instance [*ERP*](/windows).</span><span class="sxs-lookup"><span data-stu-id="b0118-105">A WS-Management protocol element returned in an enumeration that obtains both the instances and the instance [*EPRs*](/windows).</span></span> <span data-ttu-id="b0118-106">**WSMan : items** est un conteneur qui contient une instance et son EPR.</span><span class="sxs-lookup"><span data-stu-id="b0118-106">**wsman:Items** is a container that holds an instance and its EPR.</span></span> <span data-ttu-id="b0118-107">Ce type d’énumération est initié lorsque l’indicateur **WSManFlagReturnObjectAndEPR** est défini dans la demande.</span><span class="sxs-lookup"><span data-stu-id="b0118-107">This type of enumeration is initiated when the **WSManFlagReturnObjectAndEPR** flag is set in the request.</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="b0118-108">B</span><span class="sxs-lookup"><span data-stu-id="b0118-108">B</span></span>

<dl> <dt>

<span data-ttu-id="b0118-109">**contrôleur BMC (Baseboard Management Controller)**</span><span class="sxs-lookup"><span data-stu-id="b0118-109">**baseboard management controller (BMC)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-110">Microcontrôleur attaché localement à un serveur.</span><span class="sxs-lookup"><span data-stu-id="b0118-110">A microcontroller attached locally to a server.</span></span> <span data-ttu-id="b0118-111">Les contrôleurs BMC ont des capteurs qui surveillent l’état physique du serveur et une connexion réseau distincte qui peut communiquer sur le réseau, même si le serveur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b0118-111">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="b0118-112">Vous avez accès aux données BMC via le fournisseur WMI [*de l’interface de gestion de plateforme intelligente (IPMI)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-112">You have access to BMC data through the [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md) WMI provider.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-113">**Authentification de base**</span><span class="sxs-lookup"><span data-stu-id="b0118-113">**Basic authentication**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-114">Nom d’utilisateur et mot de passe envoyés dans l’échange d’authentification.</span><span class="sxs-lookup"><span data-stu-id="b0118-114">The user name and password sent in the authentication exchange.</span></span> <span data-ttu-id="b0118-115">L’authentification de base peut être configurée pour utiliser le transport HTTP ou HTTPs dans un domaine ou un groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="b0118-115">Basic authentication can be configured to use either HTTP or HTTPS transport in a domain or workgroup.</span></span> <span data-ttu-id="b0118-116">Cette méthode est la méthode d'authentification la moins sécurisée.</span><span class="sxs-lookup"><span data-stu-id="b0118-116">This method is the least secure method of authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-117">**BMC**</span><span class="sxs-lookup"><span data-stu-id="b0118-117">**BMC**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-118">Consultez [*Baseboard Management Controller (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-118">See [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="b0118-119">C</span><span class="sxs-lookup"><span data-stu-id="b0118-119">C</span></span>

<dl> <dt>

<span data-ttu-id="b0118-120">**MODÈLE**</span><span class="sxs-lookup"><span data-stu-id="b0118-120">**CIM**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-121">Voir [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-121">See [*Common Information Model (CIM)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-122">**client**</span><span class="sxs-lookup"><span data-stu-id="b0118-122">**client**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-123">L’application cliente qui utilise le protocole WS-Management pour accéder au service de gestion sur l’ordinateur local ou distant.</span><span class="sxs-lookup"><span data-stu-id="b0118-123">The client application using the WS-Management protocol to access the management service on either the local or a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-124">**Common Information Model (CIM)**</span><span class="sxs-lookup"><span data-stu-id="b0118-124">**Common Information Model (CIM)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-125">Le modèle [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md) qui décrit comment représenter des objets ordinateur et réseau réels.</span><span class="sxs-lookup"><span data-stu-id="b0118-125">The [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md) model that describes how to represent real-world computer and network objects.</span></span> <span data-ttu-id="b0118-126">CIM utilise un paradigme orienté objet, où les objets managés sont modelés à l'aide des concepts de classes et d'instances.</span><span class="sxs-lookup"><span data-stu-id="b0118-126">CIM uses an object-oriented paradigm, where managed objects are modeled using the concepts of classes and instances.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="b0118-127">D</span><span class="sxs-lookup"><span data-stu-id="b0118-127">D</span></span>

<dl> <dt>

<span data-ttu-id="b0118-128">**Authentification Digest**</span><span class="sxs-lookup"><span data-stu-id="b0118-128">**Digest authentication**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-129">Échange sur lequel le serveur reçoit une demande d’un client et envoie des données sur le client à un serveur d’authentification, généralement un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="b0118-129">An exchange wherein the server receives a request from a client and sends data about the client to an authenticating server, typically a domain controller.</span></span> <span data-ttu-id="b0118-130">Si le client est authentifié, le serveur reçoit une clé de session Digest utilisée pour authentifier les demandes ultérieures du client.</span><span class="sxs-lookup"><span data-stu-id="b0118-130">If the client is authenticated, then the server receives a Digest session key used to authenticate subsequent requests from the client.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-131">**DMTF (Distributed Management Task Force)**</span><span class="sxs-lookup"><span data-stu-id="b0118-131">**Distributed Management Task Force (DMTF)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-132">L’organisation de l’industrie développant les normes de gestion et la technologie d’intégration pour les environnements d’entreprise et Internet.</span><span class="sxs-lookup"><span data-stu-id="b0118-132">The industry organization developing management standards and integration technology for enterprise and Internet environments.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-133">**DMTF**</span><span class="sxs-lookup"><span data-stu-id="b0118-133">**DMTF**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-134">Voir [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-134">See [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="b0118-135">E</span><span class="sxs-lookup"><span data-stu-id="b0118-135">E</span></span>

<dl> <dt>

<span data-ttu-id="b0118-136">**endpoint**</span><span class="sxs-lookup"><span data-stu-id="b0118-136">**endpoint**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-137">Ressource qui peut être traitée par une [*référence de point de terminaison (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-137">A resource that can be addressed by an [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-138">**Référence du point de terminaison (EPR)**</span><span class="sxs-lookup"><span data-stu-id="b0118-138">**endpoint reference (EPR)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-139">Combinaison de WS-Addressing et WS-Management éléments d’adressage qui décrivent ensemble une adresse pour une ressource dans l’en-tête SOAP du message.</span><span class="sxs-lookup"><span data-stu-id="b0118-139">A combination of WS-Addressing and WS-Management addressing elements that together describe an address for a resource in the message SOAP header.</span></span> <span data-ttu-id="b0118-140">Il s’agit d’un terme de service Web.</span><span class="sxs-lookup"><span data-stu-id="b0118-140">This is a web service term.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-141">**énumération**</span><span class="sxs-lookup"><span data-stu-id="b0118-141">**enumeration**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-142">Un ensemble ou une collection d’instances de [*ressource*](windows-remote-management-glossary.md) ou l’action de demander un tel ensemble.</span><span class="sxs-lookup"><span data-stu-id="b0118-142">A set, or collection, of [*resource*](windows-remote-management-glossary.md) instances or the action of requesting such a set.</span></span> <span data-ttu-id="b0118-143">Dans WS-Management protocole, [*WS-Enumeration*](windows-remote-management-glossary.md) est utilisé pour obtenir la collection.</span><span class="sxs-lookup"><span data-stu-id="b0118-143">In WS-Management protocol, [*WS-Enumeration*](windows-remote-management-glossary.md) is used to obtain the collection.</span></span> <span data-ttu-id="b0118-144">Dans l’implémentation de script de service WinRM de l’énumération, [**session. Enumerate**](session-enumerate.md) et l’objet [**énumérateur**](enumerator.md) sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="b0118-144">In the WinRM service scripting implementation of enumeration, [**Session.Enumerate**](session-enumerate.md) and the [**Enumerator**](enumerator.md) object are used.</span></span> <span data-ttu-id="b0118-145">La méthode et l’interface C++ correspondantes sont [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) et [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="b0118-145">The corresponding C++ method and interface are [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate) and [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-146">**EPR**</span><span class="sxs-lookup"><span data-stu-id="b0118-146">**EPR**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-147">Consultez [*Référence du point de terminaison (EPR)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-147">See [*endpoint reference (EPR)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-148">**Service de collecte d’événements**</span><span class="sxs-lookup"><span data-stu-id="b0118-148">**Event Collection Service**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-149">Composant du système d’exploitation qui reçoit les événements du BMC et d’autres composants ou applications du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0118-149">The operating system component that receives events from the BMC and other operating system components or applications.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-150">**transfert d’événements**</span><span class="sxs-lookup"><span data-stu-id="b0118-150">**event forwarding**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-151">Une notification d’événements qui se produisent sur des ordinateurs distants peut être envoyée aux applications d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0118-151">A notification of events that occur on remote computers can be sent to subscribing applications.</span></span> <span data-ttu-id="b0118-152">Le transfert d’événements n’est pas une fonctionnalité de WinRM, mais du [Journal des événements Windows](/windows/desktop/WES/windows-event-log).</span><span class="sxs-lookup"><span data-stu-id="b0118-152">Event forwarding is not a feature of WinRM, but of the [Windows Event Log](/windows/desktop/WES/windows-event-log).</span></span> <span data-ttu-id="b0118-153">Le transfert d’événements devient disponible pour la première fois dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0118-153">Event forwarding becomes available for the first time in Windows Vista.</span></span> <span data-ttu-id="b0118-154">Les applications de gestion, telles que les Microsoft Operations Manager (MOM) utilisent le transfert d’événements.</span><span class="sxs-lookup"><span data-stu-id="b0118-154">The Management applications, such as Microsoft Operations Manager (MOM) use event forwarding.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="b0118-155">F</span><span class="sxs-lookup"><span data-stu-id="b0118-155">F</span></span>

<dl> <dt>

<span data-ttu-id="b0118-156">**filter**</span><span class="sxs-lookup"><span data-stu-id="b0118-156">**filter**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-157">Mécanisme de requête permettant de spécifier un ensemble limité d’instances dans la demande d’une [*ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-157">A query mechanism for specifying a limited set of instances in the request for a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-158">Vous pouvez spécifier un paramètre de *filtre* sur les appels à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="b0118-158">You can specify a *filter* parameter on calls to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-159">**dialecte de filtre**</span><span class="sxs-lookup"><span data-stu-id="b0118-159">**filter dialect**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-160">Chaîne XML qui identifie le dialecte XML utilisé pour spécifier un [*filtre*](windows-remote-management-glossary.md) dans un appel à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="b0118-160">An XML string that identifies the XML dialect used to specify a [*filter*](windows-remote-management-glossary.md) in a call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span> <span data-ttu-id="b0118-161">Le service WinRM prend en charge [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) comme dialecte de filtre lors de la réception des demandes.</span><span class="sxs-lookup"><span data-stu-id="b0118-161">The WinRM service supports [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi) as a filter dialect when receiving requests.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-162">**échantillon**</span><span class="sxs-lookup"><span data-stu-id="b0118-162">**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-163">Chaîne XML qui identifie une partie d’une instance d’une ressource plutôt que l’intégralité de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b0118-163">An XML string that identifies part of an instance of a resource rather than the entire resource.</span></span> <span data-ttu-id="b0118-164">La prise en charge des fragments est trouvée dans l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-164">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-165">**dialecte de fragment**</span><span class="sxs-lookup"><span data-stu-id="b0118-165">**fragment dialect**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-166">Chaîne XML qui identifie le dialecte XML utilisé pour spécifier un [*fragment*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-166">An XML string that identifies the XML dialect used to specify a [*fragment*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-167">La prise en charge des fragments est trouvée dans l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-167">Fragment support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="b0118-168">Le service WinRM prend en charge [*XPath*](windows-remote-management-glossary.md) pour le dialecte de fragment lors de la réception des demandes.</span><span class="sxs-lookup"><span data-stu-id="b0118-168">The WinRM service supports [*XPath*](windows-remote-management-glossary.md) for fragment dialect when receiving requests.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="b0118-169">I</span><span class="sxs-lookup"><span data-stu-id="b0118-169">I</span></span>

<dl> <dt>

<span data-ttu-id="b0118-170">**intrabande**</span><span class="sxs-lookup"><span data-stu-id="b0118-170">**in-band**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-171">L’application cliente obtient les données BMC via l' [*écouteur*](windows-remote-management-glossary.md) WinRM dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0118-171">The client application obtains BMC data through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-172">**Interface de gestion de plateforme intelligente (IPMI)**</span><span class="sxs-lookup"><span data-stu-id="b0118-172">**Intelligent Platform Management Interface (IPMI)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-173">Une norme de l’industrie informatique pour l’architecture du [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-173">An IT industry standard for the architecture of [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-174">Les fonctionnalités de gestion du matériel Windows fournissent un [*pilote IPMI*](windows-remote-management-glossary.md) et un [*fournisseur IPMI*](windows-remote-management-glossary.md) WMI qui permettent aux scripts de gestion, aux outils en ligne de commande et aux applications d’obtenir des données BMC.</span><span class="sxs-lookup"><span data-stu-id="b0118-174">The Windows hardware management features supply an [*IPMI driver*](windows-remote-management-glossary.md) and a WMI [*IPMI provider*](windows-remote-management-glossary.md) that allow management scripts, command-line tools, and applications to obtain BMC data.</span></span> <span data-ttu-id="b0118-175">Le fournisseur IPMI a des [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)WMI.</span><span class="sxs-lookup"><span data-stu-id="b0118-175">The IPMI provider has WMI [classes](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-176">**IPMI**</span><span class="sxs-lookup"><span data-stu-id="b0118-176">**IPMI**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-177">Voir [*interface de gestion de plateforme intelligente (IMPI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-177">See [*Intelligent Platform Management Interface (IMPI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-178">**Pilote IPMI**</span><span class="sxs-lookup"><span data-stu-id="b0118-178">**IPMI driver**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-179">Pilote du noyau qui permet d’accéder aux périphériques du contrôleur de gestion de la carte de configuration [*(BMC)*](windows-remote-management-glossary.md) à partir des composants du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0118-179">The kernel driver that enables access to [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) devices from the operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-180">**Fournisseur IPMI**</span><span class="sxs-lookup"><span data-stu-id="b0118-180">**IPMI provider**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-181">Fournisseur WMI standard qui définit les classes de modélisation de l' [*interface IPMI*](windows-remote-management-glossary.md) et de ses données.</span><span class="sxs-lookup"><span data-stu-id="b0118-181">A standard WMI provider that defines classes modeling the [*IPMI*](windows-remote-management-glossary.md) and its data.</span></span> <span data-ttu-id="b0118-182">Le [fournisseur IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) est une dll com qui obtient des données à partir du BMC.</span><span class="sxs-lookup"><span data-stu-id="b0118-182">The [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) is a COM DLL that obtains data from the BMC.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="b0118-183">K</span><span class="sxs-lookup"><span data-stu-id="b0118-183">K</span></span>

<dl> <dt>

<span data-ttu-id="b0118-184">**KCS**</span><span class="sxs-lookup"><span data-stu-id="b0118-184">**KCS**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-185">Voir [*style de contrôleur clavier (KCS)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-185">See [*Keyboard Controller Style (KCS)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-186">**Authentification Kerberos**</span><span class="sxs-lookup"><span data-stu-id="b0118-186">**Kerberos authentication**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-187">Méthode d’authentification mutuelle entre le client et le serveur qui utilise des clés chiffrées.</span><span class="sxs-lookup"><span data-stu-id="b0118-187">A method of mutual authentication between the client and server that uses encrypted keys.</span></span> <span data-ttu-id="b0118-188">Pour les ordinateurs qui s’exécutent sur un système d’exploitation Windows, le compte client doit être un compte de domaine dans le même domaine que le serveur.</span><span class="sxs-lookup"><span data-stu-id="b0118-188">For computers running on a Windows-based operating system, the client account must be a domain account in the same domain as the server.</span></span> <span data-ttu-id="b0118-189">Lorsqu’un client utilise des informations d’identification par défaut, Kerberos est la méthode d’authentification si la chaîne de connexion ne correspond pas à l’un des éléments suivants : localhost, 127.0.0.1 ou \[ :: 1 \] .</span><span class="sxs-lookup"><span data-stu-id="b0118-189">When a client uses default credentials, Kerberos is the authentication method if the connection string is not one of the following: localhost, 127.0.0.1, or \[::1\].</span></span>

</dd> <dt>

<span data-ttu-id="b0118-190">**Style de contrôleur de clavier (KCS)**</span><span class="sxs-lookup"><span data-stu-id="b0118-190">**Keyboard Controller Style (KCS)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-191">Protocole utilisé par le [*pilote IPMI*](windows-remote-management-glossary.md) pour communiquer avec le [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-191">The protocol used by the [*IPMI driver*](windows-remote-management-glossary.md) to communicate with the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="b0118-192">L</span><span class="sxs-lookup"><span data-stu-id="b0118-192">L</span></span>

<dl> <dt>

<span data-ttu-id="b0118-193">**listener**</span><span class="sxs-lookup"><span data-stu-id="b0118-193">**listener**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-194">Service de gestion qui implémente WS-Management protocole pour envoyer et recevoir des messages.</span><span class="sxs-lookup"><span data-stu-id="b0118-194">A management service that implements WS-Management protocol to send and receive messages.</span></span> <span data-ttu-id="b0118-195">WinRM est un service d’écoute.</span><span class="sxs-lookup"><span data-stu-id="b0118-195">WinRM is a listener service.</span></span> <span data-ttu-id="b0118-196">Un écouteur est défini par un transport (HTTP ou HTTPs) et une adresse IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="b0118-196">A listener is defined by a transport (HTTP or HTTPS) and an IPv4 or IPv6 address.</span></span> <span data-ttu-id="b0118-197">Vous pouvez créer plusieurs instances de l’écouteur WinRM sur un seul ordinateur en leur attribuant une adresse TCP/IP ou un numéro de port différent.</span><span class="sxs-lookup"><span data-stu-id="b0118-197">You can create more than one WinRM listener instance on a single computer by giving them a different TCP/IP address or port number.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="b0118-198">M</span><span class="sxs-lookup"><span data-stu-id="b0118-198">M</span></span>

<dl> <dt>

<span data-ttu-id="b0118-199">**message**</span><span class="sxs-lookup"><span data-stu-id="b0118-199">**message**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-200">Un package d’informations transmises entre des ordinateurs ou des réseaux distincts construits à l’aide du protocole [*SOAP*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-200">A package of information transmitted between computers or separate networks constructed with the [*SOAP*](windows-remote-management-glossary.md) protocol.</span></span> <span data-ttu-id="b0118-201">Le package possède un en-tête, qui décrit la cible et le transport du message, ainsi qu’un corps qui contient le contenu à utiliser lors de l’arrivée du message.</span><span class="sxs-lookup"><span data-stu-id="b0118-201">The package has a header, that describes the message target and transport, and a body that contains the content to be used when the message arrives.</span></span> <span data-ttu-id="b0118-202">Un message est une combinaison d’éléments provenant de spécifications telles que [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md)et [*WS-Management*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-202">A message is a combination of elements from specifications such as [*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Transfer*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="b0118-203">N</span><span class="sxs-lookup"><span data-stu-id="b0118-203">N</span></span>

<dl> <dt>

<span data-ttu-id="b0118-204">**namespace**</span><span class="sxs-lookup"><span data-stu-id="b0118-204">**namespace**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-205">Un espace de noms [*WMI*](windows-remote-management-glossary.md) , qui est un regroupement logique de classes et d’instances WMI pour contrôler l’étendue et l’accès.</span><span class="sxs-lookup"><span data-stu-id="b0118-205">A [*WMI*](windows-remote-management-glossary.md) namespace, which is a logical grouping of WMI classes and instances to control scope and access.</span></span> <span data-ttu-id="b0118-206">La source de données de gestion la plus fréquente pour les systèmes exécutant Windows est l' \\ espace de noms CIMV2 racine, qui contient des classes telles que le [**\_ processus Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="b0118-206">The most frequent source of management data for systems running Windows is the root\\cimv2 namespace, which contains classes such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span> <span data-ttu-id="b0118-207">Les espaces de noms apparaissent dans l’URI de ressource pour les classes WMI, par exemple https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service .</span><span class="sxs-lookup"><span data-stu-id="b0118-207">Namespaces appear in the resource URI for WMI classes, for example https://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-208">**Négocier l’authentification**</span><span class="sxs-lookup"><span data-stu-id="b0118-208">**Negotiate authentication**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-209">Type d’authentification unique négocié, qui est l’implémentation Windows d’un mécanisme de [*négociation GSSAPI simple et protégé (SPNEGO)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-209">A negotiated, single sign on type of authentication that is the Windows implementation of [*Simple and Protected GSSAPI Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-210">La négociation SPNEGO détermine si l’authentification est gérée par Kerberos ou NTLM.</span><span class="sxs-lookup"><span data-stu-id="b0118-210">SPNEGO negotiation determines whether authentication is handled by Kerberos or NTLM.</span></span> <span data-ttu-id="b0118-211">Kerberos est le mécanisme préféré.</span><span class="sxs-lookup"><span data-stu-id="b0118-211">Kerberos is the preferred mechanism.</span></span> <span data-ttu-id="b0118-212">L’authentification par négociation sur les systèmes Windows est également appelée authentification intégrée de Windows.</span><span class="sxs-lookup"><span data-stu-id="b0118-212">Negotiate authentication on Windows-based systems is also called Windows Integrated Authentication.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-213">**capteur numérique**</span><span class="sxs-lookup"><span data-stu-id="b0118-213">**numeric sensor**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-214">Type numérique de capteur dans un contrôleur de gestion de la [*carte de baseboard (BMC)*](windows-remote-management-glossary.md), par exemple la température ou la tension.</span><span class="sxs-lookup"><span data-stu-id="b0118-214">A numeric type of sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md), for example temperature or voltage.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="b0118-215">O</span><span class="sxs-lookup"><span data-stu-id="b0118-215">O</span></span>

<dl> <dt>

<span data-ttu-id="b0118-216">**option**</span><span class="sxs-lookup"><span data-stu-id="b0118-216">**option**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-217">Données supplémentaires requises par le fournisseur de ressources pour traiter une demande.</span><span class="sxs-lookup"><span data-stu-id="b0118-217">The additional data required by the resource provider to process a request.</span></span> <span data-ttu-id="b0118-218">Par exemple, certains fournisseurs WMI requièrent des données supplémentaires fournies sous forme d’objets [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) .</span><span class="sxs-lookup"><span data-stu-id="b0118-218">For example, some WMI providers require additional data supplied as [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) objects.</span></span> <span data-ttu-id="b0118-219">La prise en charge des options se trouve dans l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-219">Option support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-220">**hors bande**</span><span class="sxs-lookup"><span data-stu-id="b0118-220">**out-of-band**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-221">L’application cliente obtient les données directement à partir du contrôleur de gestion de la carte de configuration [*(BMC)*](windows-remote-management-glossary.md) d’un autre ordinateur, plutôt que via l' [*écouteur*](windows-remote-management-glossary.md) WinRM dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0118-221">The client application obtains data directly from the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) of another computer, rather than through the WinRM [*listener*](windows-remote-management-glossary.md) in the operating system.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="b0118-222">P</span><span class="sxs-lookup"><span data-stu-id="b0118-222">P</span></span>

<dl> <dt>

<span data-ttu-id="b0118-223">**collecter**</span><span class="sxs-lookup"><span data-stu-id="b0118-223">**pull**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-224">Un message d’extraction [*WS-Enumeration*](windows-remote-management-glossary.md) est envoyé pour continuer une énumération démarrée par un appel initial à WS-Enumeration : Enumerate.</span><span class="sxs-lookup"><span data-stu-id="b0118-224">A [*WS-Enumeration*](windows-remote-management-glossary.md) pull message is sent to continue an enumeration started by an initial call to WS-Enumeration:Enumerate.</span></span> <span data-ttu-id="b0118-225">L’opération d’extraction dans le service WinRM est effectuée par [**Enumerator. ReadItem**](enumerator-readitem.md) ou [**IWSManEnumerator :: ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span><span class="sxs-lookup"><span data-stu-id="b0118-225">The pull operation in the WinRM service is performed by [**Enumerator.ReadItem**](enumerator-readitem.md) or [**IWSManEnumerator::ReadItem**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanenumerator-readitem).</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="b0118-226">R</span><span class="sxs-lookup"><span data-stu-id="b0118-226">R</span></span>

<dl> <dt>

<span data-ttu-id="b0118-227">**resource**</span><span class="sxs-lookup"><span data-stu-id="b0118-227">**resource**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-228">[*Point de terminaison*](windows-remote-management-glossary.md) qui représente un type distinct d’opération ou de valeur de gestion.</span><span class="sxs-lookup"><span data-stu-id="b0118-228">An [*endpoint*](windows-remote-management-glossary.md) that represents a distinct type of management operation or value.</span></span> <span data-ttu-id="b0118-229">Un service expose une ou plusieurs ressources et certaines ressources peuvent avoir plusieurs instances.</span><span class="sxs-lookup"><span data-stu-id="b0118-229">A service exposes one or more resources and some resources can have more than one instance.</span></span> <span data-ttu-id="b0118-230">Une ressource de gestion est semblable à une classe WMI ou à une table de base de données, et une instance est semblable à une instance de la classe ou à une ligne de la table.</span><span class="sxs-lookup"><span data-stu-id="b0118-230">A management resource is similar to a WMI class or a database table, and an instance is similar to an instance of the class or a row in the table.</span></span> <span data-ttu-id="b0118-231">Par exemple, la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="b0118-231">For example, the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class represents a resource.</span></span> <span data-ttu-id="b0118-232">`Win32_LogicalDisk="C:\"` est une instance spécifique de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b0118-232">`Win32_LogicalDisk="C:\"` is a specific instance of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-233">**URI de ressource**</span><span class="sxs-lookup"><span data-stu-id="b0118-233">**resource URI**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-234">L' [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md) utilisé pour identifier un type spécifique de ressource, tel que des disques ou des processus, sur un système.</span><span class="sxs-lookup"><span data-stu-id="b0118-234">The [*uniform resource identifier (URI)*](windows-remote-management-glossary.md) used to identify a specific type of resource, such as disks or processes, on a system.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="b0118-235">S</span><span class="sxs-lookup"><span data-stu-id="b0118-235">S</span></span>

<dl> <dt>

<span data-ttu-id="b0118-236">**SÉLECTION**</span><span class="sxs-lookup"><span data-stu-id="b0118-236">**SEL**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-237">Consultez [*Journal des événements système (sel)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-237">See [*System Event Log (SEL)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-238">**Adaptateur SEL**</span><span class="sxs-lookup"><span data-stu-id="b0118-238">**SEL adapter**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-239">Adaptateur qui envoie les données du [*contrôleur BMC (Baseboard Management Controller)*](windows-remote-management-glossary.md) au [*collecteur d’événements*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-239">The adapter that sends [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) data to the [*Event Collector*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-240">**sélection**</span><span class="sxs-lookup"><span data-stu-id="b0118-240">**selector**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-241">Paire nom/valeur qui représente une instance particulière d’une [*ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-241">A name and value pair that represents a particular instance of a [*resource*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-242">Il s’agit essentiellement d’un filtre ou d’une « clé » qui identifie l’instance souhaitée de la ressource.</span><span class="sxs-lookup"><span data-stu-id="b0118-242">This is essentially a filter or "key" that identifies the desired instance of the resource.</span></span> <span data-ttu-id="b0118-243">La prise en charge du sélecteur se trouve dans l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-243">Selector support is found in the [**ResourceLocator**](resourcelocator.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-244">**capteur**</span><span class="sxs-lookup"><span data-stu-id="b0118-244">**sensor**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-245">Un appareil de mesure dans un contrôleur de gestion de la [*carte de baseboard (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-245">A measurement device in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-246">**service**</span><span class="sxs-lookup"><span data-stu-id="b0118-246">**service**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-247">Application qui fournit des services de gestion aux clients via le protocole WS-Management et d’autres [*services Web*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-247">An application that provides management services to clients through the WS-Management protocol and other [*web services*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-248">Un service est généralement identique à l' [*écouteur*](windows-remote-management-glossary.md) d’un réseau.</span><span class="sxs-lookup"><span data-stu-id="b0118-248">A service is usually the same as the [*listener*](windows-remote-management-glossary.md) on a network.</span></span> <span data-ttu-id="b0118-249">Le service a une adresse de transport physique.</span><span class="sxs-lookup"><span data-stu-id="b0118-249">The service has a physical transport address.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-250">**session**</span><span class="sxs-lookup"><span data-stu-id="b0118-250">**session**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-251">Une connexion entre un Windows Remote Management [*client*](windows-remote-management-glossary.md) et l' [*écouteur*](windows-remote-management-glossary.md)WinRM local ou distant, ou le service.</span><span class="sxs-lookup"><span data-stu-id="b0118-251">A connection between a Windows Remote Management [*client*](windows-remote-management-glossary.md) and the local or remote WinRM [*listener*](windows-remote-management-glossary.md), or service.</span></span> <span data-ttu-id="b0118-252">Cette connexion est semblable à la connexion entre un script client WMI et WMI sur un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="b0118-252">This connection is similar to the connection between a WMI client script and WMI on a remote server.</span></span> <span data-ttu-id="b0118-253">Les opérations de session, telles que l’énumération d’une ressource (énumération), l’obtention d’une instance d’une ressource (obtenir) ou l’exécution d’une méthode de ressource (Invoke) sont des méthodes de l’objet de **session** .</span><span class="sxs-lookup"><span data-stu-id="b0118-253">The session operations, such as enumerating a resource (Enumerate), getting an instance of a resource (Get), or running a resource method (Invoke) are methods of the **Session** object.</span></span> <span data-ttu-id="b0118-254">Un objet de **session** est créé par [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-254">A **Session** object is created by [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-255">**Interface SPNEGO (simple and Protected GSS-API Negotiation Mechanism)**</span><span class="sxs-lookup"><span data-stu-id="b0118-255">**Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-256">Mécanisme d’authentification utilisé par le client ou le serveur pour recevoir des demandes de données via le WinRM dans un contexte de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b0118-256">An authentication mechanism used by the client or server receiving requests for data through the WinRM in an Active Directory context.</span></span> <span data-ttu-id="b0118-257">SPNEGO est basé sur un protocole RFC (Request for Comments) produit par l’IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="b0118-257">SPNEGO is based on an Request For Comments (RFC) protocol produced by the Internet Engineering Task Force (IETF).</span></span> <span data-ttu-id="b0118-258">SPNEGO est également connu sous le nom [*d’authentification intégrée de Windows*](windows-remote-management-glossary.md), le terme utilisé dans les rubriques d’aide Windows Remote Management.</span><span class="sxs-lookup"><span data-stu-id="b0118-258">SPNEGO is also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md), the term used in the Windows Remote Management help topics.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-259">**protocole SOAP (Simple Object Access Protocol) ;**</span><span class="sxs-lookup"><span data-stu-id="b0118-259">**Simple Object Access Protocol (SOAP)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-260">Protocole XML utilisé par les services Web.</span><span class="sxs-lookup"><span data-stu-id="b0118-260">An XML-based protocol used by web services.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-261">**SOAP**</span><span class="sxs-lookup"><span data-stu-id="b0118-261">**SOAP**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-262">Voir [*protocole SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-262">See [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-263">**SPNEGO**</span><span class="sxs-lookup"><span data-stu-id="b0118-263">**SPNEGO**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-264">Consultez [*le mécanisme SPNEGO (simple and Protected GSS-API Negotiation Mechanism)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-264">See [*Simple and Protected GSS-API Negotiation Mechanism (SPNEGO)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-265">**Journal des événements système (SEL)**</span><span class="sxs-lookup"><span data-stu-id="b0118-265">**System Event Log (SEL)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-266">La base de données des événements dans le matériel du contrôleur de gestion de la carte de base [*(BMC)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-266">The database of events in the [*baseboard management controller (BMC)*](windows-remote-management-glossary.md) hardware.</span></span> <span data-ttu-id="b0118-267">L' [*adaptateur sel*](windows-remote-management-glossary.md) transmet ces événements au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0118-267">The [*SEL adapter*](windows-remote-management-glossary.md) conveys these events to the operating system.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="b0118-268">U</span><span class="sxs-lookup"><span data-stu-id="b0118-268">U</span></span>

<dl> <dt>

<span data-ttu-id="b0118-269">**URI (Uniform Resource Identifier)**</span><span class="sxs-lookup"><span data-stu-id="b0118-269">**uniform resource identifier (URI)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-270">Chaîne qui identifie une ressource dans l’entreprise, telle qu’un ordinateur, un processus, un lecteur de disque ou un capteur de température dans un [*contrôleur de gestion de la carte de baseboard (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-270">A string that identifies a resource in the enterprise, such as a computer, a process, a disk drive, or a temperature sensor in a [*baseboard management controller (BMC)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-271">L’URI est le mécanisme d’adressage de service Web défini dans IETF (Internet Engineering Task Force) Uniform Resource Identifier (URI) : syntaxe générique \[ norme RFC 3986 \] .</span><span class="sxs-lookup"><span data-stu-id="b0118-271">The URI is the web service addressing mechanism defined in Internet Engineering Task Force (IETF) Uniform Resource Identifier (URI): Generic Syntax \[RFC3986\].</span></span>

</dd> <dt>

<span data-ttu-id="b0118-272">**URI**</span><span class="sxs-lookup"><span data-stu-id="b0118-272">**URI**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-273">Consultez [*URI (Uniform Resource Identifier)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-273">See [*uniform resource identifier (URI)*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

## <a name="w"></a><span data-ttu-id="b0118-274">W</span><span class="sxs-lookup"><span data-stu-id="b0118-274">W</span></span>

<dl> <dt>

<span data-ttu-id="b0118-275">**service Web**</span><span class="sxs-lookup"><span data-stu-id="b0118-275">**web service**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-276">Application logicielle utilisée pour l’interaction entre les ordinateurs sur Internet ou sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="b0118-276">A software application used for interaction between computers across the Internet or a network.</span></span> <span data-ttu-id="b0118-277">Les services Web sont décrits par le [*langage WSDL (Web Service Description Language)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-277">Web services are described by the [*Web Service Description Language (WSDL)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-278">La description spécifique du service Web indique aux autres services comment interagir avec le service Web à l’aide de messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="b0118-278">The specific description of the web service tells other services how to interact with the web service by using SOAP messages.</span></span> <span data-ttu-id="b0118-279">Les messages sont acheminés entre les ordinateurs par un transport, en général HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="b0118-279">The messages are conveyed between computers by a transport, typically HTTP or HTTPS.</span></span> <span data-ttu-id="b0118-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md)et [*WS-Management*](windows-remote-management-glossary.md) sont des exemples de protocoles utilisés par les applications de service Web pour communiquer entre elles.</span><span class="sxs-lookup"><span data-stu-id="b0118-280">[*WS-Addressing*](windows-remote-management-glossary.md), [*WS-Eventing*](windows-remote-management-glossary.md), and [*WS-Management*](windows-remote-management-glossary.md) are examples of protocols used by web service applications to communicate with each other.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-281">**WSDL (Web Service Description Language)**</span><span class="sxs-lookup"><span data-stu-id="b0118-281">**Web Service Description Language (WSDL)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-282">Langage basé sur XML utilisé pour définir le mode d’interaction avec un service Web.</span><span class="sxs-lookup"><span data-stu-id="b0118-282">An XML-based language used to define how to interact with a web service.</span></span> <span data-ttu-id="b0118-283">En général, le WSDL décrit les messages SOAP requis par le service Web pour retourner des données ou effectuer des opérations.</span><span class="sxs-lookup"><span data-stu-id="b0118-283">Typically, the WSDL describes what SOAP messages the web service requires to return data or carry out operations.</span></span> <span data-ttu-id="b0118-284">Le WSDL permet à une implémentation d’un système d’exploitation de communiquer avec le service Web implémenté sur un autre système d’exploitation, à condition que les spécifications du WSDL soient remplies.</span><span class="sxs-lookup"><span data-stu-id="b0118-284">The WSDL allows an implementation from one operating system to communicate with the web service implemented on another operating system, as long as the requirements of the WSDL are met.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-285">**Authentification Windows intégrée**</span><span class="sxs-lookup"><span data-stu-id="b0118-285">**Windows Integrated Authentication**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-286">Consultez [*négociation de l’authentification*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-286">See [*Negotiate authentication*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-287">**Windows Management Instrumentation (WMI)**</span><span class="sxs-lookup"><span data-stu-id="b0118-287">**Windows Management Instrumentation (WMI)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-288">L’implémentation Microsoft de la norme WBEM (Web-Based Enterprise Management) publiée par la [*DMTF (Distributed Management Task Force)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-288">The Microsoft implementation of the Web-Based Enterprise Management (WBEM) standard published by the [*Distributed Management Task Force (DMTF)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="b0118-289">WMI vous permet de gérer des ordinateurs locaux et distants et de modéliser des objets ordinateur et réseau à l’aide d’une extension de la norme [*Common Information Model (CIM)*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="b0118-289">WMI allows you to manage local and remote computers and models computer and network objects using an extension of the [*Common Information Model (CIM)*](windows-remote-management-glossary.md) standard.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-290">**Windows Remote Management (WinRM)**</span><span class="sxs-lookup"><span data-stu-id="b0118-290">**Windows Remote Management (WinRM)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-291">L’implémentation Microsoft d’un service Web de gestion basée sur le protocole de [*gestion des services*](windows-remote-management-glossary.md) Web standard public.</span><span class="sxs-lookup"><span data-stu-id="b0118-291">The Microsoft implementation of a management web service based on the public standard [*WS-Management*](windows-remote-management-glossary.md) protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-292">**Windows Remote Shell (WinRS)**</span><span class="sxs-lookup"><span data-stu-id="b0118-292">**Windows Remote Shell (WinRS)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-293">Outil shell qui s’appuie sur [*Windows Remote Management*](windows-remote-management-glossary.md) pour exécuter des commandes distantes, en particulier pour les serveurs headless.</span><span class="sxs-lookup"><span data-stu-id="b0118-293">A shell tool that relies on [*Windows Remote Management*](windows-remote-management-glossary.md) to execute remote commands, especially for headless servers.</span></span> <span data-ttu-id="b0118-294">L’outil en ligne de commande est Winrs.</span><span class="sxs-lookup"><span data-stu-id="b0118-294">The command-line tool is Winrs.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-295">**WMI**</span><span class="sxs-lookup"><span data-stu-id="b0118-295">**WMI**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-296">Voir [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-296">See [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0118-297">**Plug-in WMI**</span><span class="sxs-lookup"><span data-stu-id="b0118-297">**WMI plug-in**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-298">Le plug-in WinRM qui rend les données WMI disponibles pour les clients WinRM.</span><span class="sxs-lookup"><span data-stu-id="b0118-298">The WinRM plug-in that makes WMI data available to WinRM clients.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-299">**WS-Addressing (WSA)**</span><span class="sxs-lookup"><span data-stu-id="b0118-299">**WS-Addressing (wsa)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-300">Protocole public standard, qui est basé sur SOAP, qui crée un système d’adressage utilisé dans les en-têtes de messages envoyés sur Internet.</span><span class="sxs-lookup"><span data-stu-id="b0118-300">A public standard protocol, which is SOAP-based, that creates an addressing system used in the headers of messages sent across the Internet.</span></span> <span data-ttu-id="b0118-301">La norme définit la manière dont les ressources peuvent être situées sur des réseaux et des pare-feu.</span><span class="sxs-lookup"><span data-stu-id="b0118-301">The standard defines how resources can be located across networks and firewalls.</span></span> <span data-ttu-id="b0118-302">WS-Addressing est l’un des protocoles de service Web qui composent le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="b0118-302">WS-Addressing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-303">**WS-Enumeration (wsen)**</span><span class="sxs-lookup"><span data-stu-id="b0118-303">**WS-Enumeration (wsen)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-304">Protocole public standard, qui est basé sur SOAP, pour l’énumération d’une séquence d’éléments XML pouvant représenter des collections de données, des journaux ou d’autres structures d’informations linéaires.</span><span class="sxs-lookup"><span data-stu-id="b0118-304">A public standard protocol, which is SOAP-based, for enumerating a sequence of XML elements that may represent data collections, logs, or other linear information structures.</span></span> <span data-ttu-id="b0118-305">WS-Enumeration est l’un des protocoles de service Web qui composent le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="b0118-305">WS-Enumeration is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-306">**WS-Eventing (WSE)**</span><span class="sxs-lookup"><span data-stu-id="b0118-306">**WS-Eventing (wse)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-307">Protocole public standard, qui est basé sur SOAP, qui permet à un service Web (l’abonné) de s’abonner et d’accepter des messages de notification d’événement d’un autre service Web (la source de l’événement).</span><span class="sxs-lookup"><span data-stu-id="b0118-307">A public standard protocol, which is SOAP-based, that allows one web service (the subscriber) to subscribe to and accept event notification messages from another web service (the event source).</span></span> <span data-ttu-id="b0118-308">WS-Eventing est l’un des protocoles de service Web qui composent le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="b0118-308">WS-Eventing is one of the web service protocols which compose the WS-Management protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-309">**Gestion des services Web**</span><span class="sxs-lookup"><span data-stu-id="b0118-309">**WS-Management**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-310">Protocole public standard, qui est basé sur SOAP, pour le partage des données de gestion entre tous les systèmes d’exploitation, les ordinateurs et les périphériques.</span><span class="sxs-lookup"><span data-stu-id="b0118-310">A public standard protocol, which is SOAP-based, for sharing management data among all operating systems, computers, and devices.</span></span> <span data-ttu-id="b0118-311">Tous les [*messages*](windows-remote-management-glossary.md) envoyés par les composants du client ou du serveur WinRM utilisent ce protocole.</span><span class="sxs-lookup"><span data-stu-id="b0118-311">All [*messages*](windows-remote-management-glossary.md) sent by the WinRM client or server components use this protocol.</span></span>

</dd> <dt>

<span data-ttu-id="b0118-312">**WS-Transfer (wxf)**</span><span class="sxs-lookup"><span data-stu-id="b0118-312">**WS-Transfer (wxf)**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-313">Protocole public standard, qui est basé sur SOAP, pour accéder aux représentations XML des ressources basées sur les services Web via un ensemble simple de verbes, par exemple, obtenir, placer, appeler ou supprimer.</span><span class="sxs-lookup"><span data-stu-id="b0118-313">A public standard protocol, which is SOAP-based, for accessing XML representations of web service-based resources through a simple set of verbs such as Get, Put, Invoke, or Delete.</span></span> <span data-ttu-id="b0118-314">WS-Transfer définit des opérations pour l’envoi et la réception de la représentation d’une ressource particulière et des opérations pour la création ou la suppression d’une ressource et de sa représentation correspondante.</span><span class="sxs-lookup"><span data-stu-id="b0118-314">WS-Transfer defines operations for sending and receiving the representation of a particular resource and operations for creating or deleting a resource and its corresponding representation.</span></span>

</dd> </dl>

## <a name="x"></a><span data-ttu-id="b0118-315">X</span><span class="sxs-lookup"><span data-stu-id="b0118-315">X</span></span>

<dl> <dt>

<span data-ttu-id="b0118-316">**XPath**</span><span class="sxs-lookup"><span data-stu-id="b0118-316">**XPath**</span></span>
</dt> <dd>

<span data-ttu-id="b0118-317">Une notation de chemin d’accès pour l’adressage des parties d’un document XML, similaire à une URL.</span><span class="sxs-lookup"><span data-stu-id="b0118-317">A path notation for addressing parts of an XML document, similar to a URL.</span></span> <span data-ttu-id="b0118-318">Une expression XPath est une séquence d’expressions à obtenir à partir de l’emplacement actuel dans le document XML vers un autre nœud ou un ensemble de nœuds.</span><span class="sxs-lookup"><span data-stu-id="b0118-318">An XPath expression is a sequence of phrases to get from the current location in the XML document to another node or set of nodes.</span></span> <span data-ttu-id="b0118-319">Les expressions sont séparées par des barres obliques inverses (« / »).</span><span class="sxs-lookup"><span data-stu-id="b0118-319">The phrases are separated by forward-slash ("/") characters.</span></span> <span data-ttu-id="b0118-320">Le service WinRM prend en charge [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) pour le [*dialecte de fragment*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="b0118-320">The WinRM service supports [XPath](/previous-versions/dotnet/netframework-4.0/ms256115(v=vs.100)) for [*fragment dialect*](windows-remote-management-glossary.md).</span></span>

</dd> </dl>

 

 