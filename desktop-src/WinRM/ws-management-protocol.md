---
title: Protocole Gestion des services web
description: Norme publique pour l’échange à distance de données de gestion avec n’importe quel périphérique d’ordinateur qui implémente le protocole.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102305"
---
# <a name="ws-management-protocol"></a><span data-ttu-id="be042-103">Protocole Gestion des services web</span><span class="sxs-lookup"><span data-stu-id="be042-103">WS-Management Protocol</span></span>

<span data-ttu-id="be042-104">Le protocole Gestion des services Web a été développé par un groupe de fabricants de logiciels et de matériel afin de permettre l’échange à distance de données de gestion avec un appareil qui implémente ce protocole.</span><span class="sxs-lookup"><span data-stu-id="be042-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="be042-105">Standards</span><span class="sxs-lookup"><span data-stu-id="be042-105">Standards</span></span>

<span data-ttu-id="be042-106">Pour plus d’informations sur le protocole WS-Management, consultez [spécification WS-Management (Web Services for Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="be042-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="be042-107">L’objectif du protocole est de fournir la cohérence et l’interopérabilité pour les opérations de gestion sur de nombreux types d’appareils (notamment le microprogramme) et les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="be042-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="be042-108">WS-Management protocole peut être étendu à mesure que de nouvelles opérations sont identifiées par le secteur de l’informatique.</span><span class="sxs-lookup"><span data-stu-id="be042-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="be042-109">L’implémentation actuelle du protocole WS-Management est basée sur les spécifications standard suivantes : HTTPs, SOAP sur HTTP (profil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration et WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="be042-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="be042-110">Pour plus d’informations sur les normes de WS-Management et les schémas XML, consultez <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="be042-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="be042-111">Messages</span><span class="sxs-lookup"><span data-stu-id="be042-111">Messages</span></span>

<span data-ttu-id="be042-112">Le protocole WS-Management fournit une norme pour la construction de [*messages*](windows-remote-management-glossary.md) XML à l’aide de différentes normes de service Web, telles que [*WS-Addressing*](windows-remote-management-glossary.md) et [*WS-Transfer*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="be042-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="be042-113">Ces normes définissent des schémas XML pour les messages de service Web.</span><span class="sxs-lookup"><span data-stu-id="be042-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="be042-114">Les messages font référence à une [*ressource*](windows-remote-management-glossary.md) à l’aide d’un [*URI de ressource*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="be042-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="be042-115">Le protocole WS-Management ajoute un ensemble de définitions pour les valeurs et les opérations de gestion.</span><span class="sxs-lookup"><span data-stu-id="be042-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="be042-116">Par exemple, WS-Transfer définit les opérations d’extraction, de mise en place, de création et de suppression d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="be042-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="be042-117">WS-Management protocole ajoute renommer, extraction partielle et put partiel.</span><span class="sxs-lookup"><span data-stu-id="be042-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="be042-118">Les messages respectent les conventions du [*protocole SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) qui est utilisé par tous les protocoles de service Web.</span><span class="sxs-lookup"><span data-stu-id="be042-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="be042-119">L’exemple de code suivant affiche un message avec une opération d’extraction.</span><span class="sxs-lookup"><span data-stu-id="be042-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="be042-120">Cet exemple est indiqué comme une aide pour comprendre à quoi ressemble les messages sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="be042-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="be042-121">Vous n’avez pas besoin de savoir comment produire des messages SOAP.</span><span class="sxs-lookup"><span data-stu-id="be042-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="be042-122">Les messages sont assemblés par Windows Remote Management lorsque vous exécutez une commande à l’aide de l’outil de ligne de commande **WinRM** ou lorsque vous exécutez un script écrit avec l' [API de script WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="be042-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="be042-123">Le message est une demande d’obtenir l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) avec la propriété **DeviceID** « c : » à partir d’un serveur nommé ordinateur_distant.</span><span class="sxs-lookup"><span data-stu-id="be042-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="be042-124">La demande utilise le transport HTTP via le port 80.</span><span class="sxs-lookup"><span data-stu-id="be042-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="be042-125">Le compte qui envoie la demande doit se trouver dans le groupe Administrateurs local sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="be042-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="be042-126">Les caractères situés avant le signe deux-points au début de chaque balise indiquent la norme qui définit l’élément XML.</span><span class="sxs-lookup"><span data-stu-id="be042-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="be042-127">Par exemple, ` <wsa:To>` indique que l’élément to est défini par le WS-Addressing standard et `<s:Header>` indique le début du contenu d’en-tête dans un message SOAP.</span><span class="sxs-lookup"><span data-stu-id="be042-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="be042-128">Sachez que la majeure partie du message est composée d’éléments XML définis par SOAP ou WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="be042-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="be042-129">WS-Management protocole ajoute MaxEnvelopeSize, Selector et SelectorSet.</span><span class="sxs-lookup"><span data-stu-id="be042-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a><span data-ttu-id="be042-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be042-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be042-131">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="be042-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="be042-132">Gestion matérielle à distance</span><span class="sxs-lookup"><span data-stu-id="be042-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 