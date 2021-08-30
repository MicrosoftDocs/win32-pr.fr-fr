---
description: L’objectif de l’algorithme Diffie-Hellman est de permettre à deux hôtes ou plus de créer et de partager une clé de chiffrement secrète identique, en partageant simplement des informations sur un réseau qui n’est pas sécurisé.
ms.assetid: f89a1268-e364-41ec-a6a8-1f6331dbb787
title: Algorithmes de fournisseur Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d432a533c1f863aa9f3495f0f38147800246812b1f10bb8a728a650548b4a89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100839"
---
# <a name="diffie-hellmanschannel-provider-algorithms"></a>Algorithmes de fournisseur Diffie-Hellman/Schannel

L’objectif de l’algorithme Diffie-Hellman est de permettre à deux hôtes ou plus de créer et de partager une clé de chiffrement secrète identique, en partageant simplement des informations sur un réseau qui n’est pas sécurisé. Les informations qui sont partagées sur le réseau se présente sous la forme de deux valeurs constantes et d’une clé publique D-H.

Le fournisseur de services de chiffrement Schannel [*de Microsoft Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) prend en charge les algorithmes suivants.



| ID d’algorithme                  | Description                                                                                                                                           | Commentaires                                                                                                   |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| CALG \_ DH \_ DF                  | [ *Algorithme d’échange de clés* de Diffie-Hellman et de stockage](../secgloss/k-gly.md) | Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits. Longueur de clé par défaut : 512 bits.<br/> |
| CALG \_ MD5                     | Algorithme de hachage MD5.                                                                                                                                | Fourni uniquement pour le hachage.                                                                                 |
| CALG \_ DH \_ EPHEM               | Échange de clé D-H éphémère.                                                                                                                           | Longueur de clé : peut être définie, 384 bits à 512 bits par incréments de 8 bits. Longueur de clé par défaut : 512 bits.<br/> |
| CALG \_ SHA                     | Algorithme de hachage SHA.                                                                                                                                | Doit être utilisé pour les signatures DSS.                                                                           |
| CALG \_ RC2                     | Algorithme de chiffrement par bloc RC2                                                                                                                        | Longueur de clé : 40 à 88 bits.                                                                                 |
| CALG \_ RC4                     | Algorithme de chiffrement de flux RC4                                                                                                                       | Longueur de clé : 40 à 88 bits.                                                                                 |
| CALG \_ CYLINK \_ MEK<br/> | Algorithme de chiffrement DES variantes                                                                                                                      | Longueur de clé : 40 bits.                                                                                       |



 

 

 
