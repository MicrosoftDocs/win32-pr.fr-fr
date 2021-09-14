---
description: La fonction QueryContextAttributes (Digest) fournit des informations sur les paramètres actuels d’un contexte de sécurité.
ms.assetid: 36863f1d-ed4e-40ec-8831-1f8b9918f2d8
title: Interrogation des attributs de contexte de sécurité Digest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526c9e496a986f61762e663422a9d1eb939b1376
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009138"
---
# <a name="querying-digest-security-context-attributes"></a>Interrogation des attributs de contexte de sécurité Digest

La fonction [**QueryContextAttributes (Digest)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) fournit des informations sur les paramètres actuels d’un [*contexte de sécurité*](../secgloss/s-gly.md).

Microsoft Digest prend en charge l’interrogation des attributs de contexte de sécurité suivants.



| Attribut                   | Description                                                                                                                                                                                             |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| informations de clé d’SECPKG \_ attr \_ \_     | Informations relatives aux algorithmes de signature et de chiffrement utilisés.                                                                                                                                   |
| \_ \_ informations sur le package attr SECPKG \_ | Informations générales relatives à Microsoft Digest, telles que la taille de jeton maximale autorisée par le [*package de sécurité*](../secgloss/s-gly.md). |
| \_tailles d’attr SECPKG \_         | Tailles maximales autorisées pour les données liées aux messages telles que les signatures.                                                                                                                                |



 

 

 
