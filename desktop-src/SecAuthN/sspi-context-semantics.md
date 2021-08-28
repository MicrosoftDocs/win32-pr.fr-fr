---
description: Un contexte de sécurité est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Sémantique du contexte SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423ce097d1ab71cf50983285f3ca8731497ed5a9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482535"
---
# <a name="sspi-context-semantics"></a>Sémantique du contexte SSPI

Un [*contexte de sécurité*](../secgloss/s-gly.md) est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication. Cela comprend des informations telles que les identités du principal et des informations sur les clés, les chiffrements et les algorithmes utilisés. Pour l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ), un contexte de sécurité est une structure opaque créée via un échange impliquant la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) et la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Pour plus d’informations sur les attributs de contexte, consultez [spécifications de contexte](context-requirements.md).

Le modèle SSPI prend en charge trois types de contextes de sécurité.




| Type | Description | 
|------|-------------|
| <a href="connection-oriented-contexts.md">Connection</a> | Un <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> orienté connexion est le contexte de sécurité le plus courant et le plus simple à utiliser. L’appelant est responsable du format de message global et de l’emplacement des données dans le message. L’appelant est également responsable de l’emplacement des champs de sécurité concernés dans un message, tels que l’emplacement des données de signature.<br /> | 
| <a href="datagram-contexts.md">Datagramme</a> | Un contexte orienté <a href="/windows/desktop/SecGloss/d-gly"><em>datagramme</em></a>a une prise en charge supplémentaire pour la communication des datagrammes de type DCE. Il peut également être utilisé de façon générique pour une application de transport orientée datagramme.<br /><blockquote><p>[!Important]</p><p>Le package <a href="microsoft-kerberos.md">Microsoft Kerberos</a> ne prend pas en charge les contextes de datagramme en mode utilisateur à utilisateur.<br /></p></blockquote><br /> | 
| <a href="stream-contexts.md">STREAM</a> | Un contexte orienté flux est responsable du blocage et de la mise en forme des messages dans le package de sécurité. L’appelant ne s’intéresse pas à la mise en forme, mais plutôt à un flux de données brut.<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exigences de contexte](context-requirements.md)
</dt> <dt>

[Contextes orientés connexion](connection-oriented-contexts.md)
</dt> <dt>

[Contextes de datagramme](datagram-contexts.md)
</dt> <dt>

[Contextes de flux](stream-contexts.md)
</dt> </dl>

 

 
