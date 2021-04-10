---
description: Le fournisseur de services de chiffrement Microsoft RSA/SChannel prend en charge le hachage, la signature des données et la vérification de signature.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Fournisseur de services de chiffrement Microsoft RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9420849d62c0b728d8f3dbccc4210de3a1394308
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951247"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Fournisseur de services de chiffrement Microsoft RSA/Schannel

Le fournisseur de services de chiffrement Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) prend en charge le hachage, la signature des données et la vérification de signature. L’identificateur d’algorithme CALG \_ SSL3 \_ SHAMD5 est utilisé pour l’authentification du client SSL 3,0 et TLS 1,0. Ce CSP prend en charge la dérivation de clés pour les protocoles SSL2, PCT1, SSL3 et TLS1. Le [*hachage*](../secgloss/h-gly.md) se compose d’une concaténation d’un hachage MD5 avec un hachage SHA et signé avec une [*clé privée*](../secgloss/p-gly.md)RSA. Elle peut être exportée vers d’autres pays/régions.



|                |                                  |
|----------------|----------------------------------|
| Type de fournisseur : | **PROUVER \_ RSA \_ Schannel**          |
| Nom du fournisseur : | **MS \_ Def \_ RSA \_ Schannel \_ Prov** |



 

Pour plus d’informations sur les fournisseurs RSA/Schannel, voir [CSP Functions](cryptography-functions.md).

 

 
