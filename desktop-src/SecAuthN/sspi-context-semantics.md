---
description: Un contexte de sécurité est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication.
ms.assetid: 6c87448b-5b8d-4694-ac3f-be83a258fbb0
title: Sémantique du contexte SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcb604e09b1a2458ef05204aefbe754af26b210
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535511"
---
# <a name="sspi-context-semantics"></a>Sémantique du contexte SSPI

Un [*contexte de sécurité*](../secgloss/s-gly.md) est l’ensemble des attributs de sécurité et des règles en vigueur au cours d’une session de communication. Cela comprend des informations telles que les identités du principal et des informations sur les clés, les chiffrements et les algorithmes utilisés. Pour l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ), un contexte de sécurité est une structure opaque créée via un échange impliquant la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) et la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .

Pour plus d’informations sur les attributs de contexte, consultez [spécifications de contexte](context-requirements.md).

Le modèle SSPI prend en charge trois types de contextes de sécurité.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="connection-oriented-contexts.md">Connection</a></td>
<td>Un <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> orienté connexion est le contexte de sécurité le plus courant et le plus simple à utiliser. L’appelant est responsable du format de message global et de l’emplacement des données dans le message. L’appelant est également responsable de l’emplacement des champs de sécurité concernés dans un message, tels que l’emplacement des données de signature.<br/></td>
</tr>
<tr class="even">
<td><a href="datagram-contexts.md">Datagramme</a></td>
<td>Un contexte orienté <a href="/windows/desktop/SecGloss/d-gly"><em>datagramme</em></a>a une prise en charge supplémentaire pour la communication des datagrammes de type DCE. Il peut également être utilisé de façon générique pour une application de transport orientée datagramme.<br/>
<blockquote>
<p>[!Important]</p>
<p>Le package <a href="microsoft-kerberos.md">Microsoft Kerberos</a> ne prend pas en charge les contextes de datagramme en mode utilisateur à utilisateur.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="stream-contexts.md">Stream</a></td>
<td>Un contexte orienté flux est responsable du blocage et de la mise en forme des messages dans le package de sécurité. L’appelant ne s’intéresse pas à la mise en forme, mais plutôt à un flux de données brut.<br/></td>
</tr>
</tbody>
</table>



 

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

 

 
