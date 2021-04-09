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
# <a name="ws-management-protocol"></a>Protocole Gestion des services web

Le protocole Gestion des services Web a été développé par un groupe de fabricants de logiciels et de matériel afin de permettre l’échange à distance de données de gestion avec un appareil qui implémente ce protocole.

## <a name="standards"></a>Standards

Pour plus d’informations sur le protocole WS-Management, consultez [spécification WS-Management (Web Services for Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

L’objectif du protocole est de fournir la cohérence et l’interopérabilité pour les opérations de gestion sur de nombreux types d’appareils (notamment le microprogramme) et les systèmes d’exploitation. WS-Management protocole peut être étendu à mesure que de nouvelles opérations sont identifiées par le secteur de l’informatique.

L’implémentation actuelle du protocole WS-Management est basée sur les spécifications standard suivantes : HTTPs, SOAP sur HTTP (profil WS-I), SOAP 1,2, WS-Addressing, WS-Transfer, WS-Enumeration et WS-Eventing. Pour plus d’informations sur les normes de WS-Management et les schémas XML, consultez <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Messages

Le protocole WS-Management fournit une norme pour la construction de [*messages*](windows-remote-management-glossary.md) XML à l’aide de différentes normes de service Web, telles que [*WS-Addressing*](windows-remote-management-glossary.md) et [*WS-Transfer*](windows-remote-management-glossary.md). Ces normes définissent des schémas XML pour les messages de service Web. Les messages font référence à une [*ressource*](windows-remote-management-glossary.md) à l’aide d’un [*URI de ressource*](windows-remote-management-glossary.md). Le protocole WS-Management ajoute un ensemble de définitions pour les valeurs et les opérations de gestion. Par exemple, WS-Transfer définit les opérations d’extraction, de mise en place, de création et de suppression d’une ressource. WS-Management protocole ajoute renommer, extraction partielle et put partiel.

Les messages respectent les conventions du [*protocole SOAP (Simple Object Access Protocol)*](windows-remote-management-glossary.md) qui est utilisé par tous les protocoles de service Web.

L’exemple de code suivant affiche un message avec une opération d’extraction. Cet exemple est indiqué comme une aide pour comprendre à quoi ressemble les messages sous-jacents. Vous n’avez pas besoin de savoir comment produire des messages SOAP. Les messages sont assemblés par Windows Remote Management lorsque vous exécutez une commande à l’aide de l’outil de ligne de commande **WinRM** ou lorsque vous exécutez un script écrit avec l' [API de script WinRM](winrm-scripting-api.md).

Le message est une demande d’obtenir l’instance du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) avec la propriété **DeviceID** « c : » à partir d’un serveur nommé ordinateur_distant. La demande utilise le transport HTTP via le port 80. Le compte qui envoie la demande doit se trouver dans le groupe Administrateurs local sur l’ordinateur distant.

Les caractères situés avant le signe deux-points au début de chaque balise indiquent la norme qui définit l’élément XML. Par exemple, ` <wsa:To>` indique que l’élément to est défini par le WS-Addressing standard et `<s:Header>` indique le début du contenu d’en-tête dans un message SOAP. Sachez que la majeure partie du message est composée d’éléments XML définis par SOAP ou WS-Addressing. WS-Management protocole ajoute MaxEnvelopeSize, Selector et SelectorSet.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Gestion matérielle à distance](remote-hardware-management.md)
</dt> </dl>

 

 