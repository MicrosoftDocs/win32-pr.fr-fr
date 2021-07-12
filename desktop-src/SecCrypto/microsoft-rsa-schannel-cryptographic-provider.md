---
description: Le fournisseur de services de chiffrement Microsoft RSA/SChannel prend en charge le hachage, la signature des données et la vérification de signature.
ms.assetid: 34ede85a-579f-400f-a53e-e40711fcaaf3
title: Fournisseur de services de chiffrement Microsoft RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e1971f59911b36c3812a4508530a5e1801194
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581967"
---
# <a name="microsoft-rsaschannel-cryptographic-provider"></a>Fournisseur de services de chiffrement Microsoft RSA/Schannel

Le fournisseur de services de chiffrement Microsoft [*RSA*](../secgloss/r-gly.md) / [*Schannel*](../secgloss/s-gly.md) prend en charge le hachage, la signature des données et la vérification de signature. L’identificateur d’algorithme CALG \_ SSL3 \_ SHAMD5 est utilisé pour l’authentification du client SSL 3,0 et TLS 1,0. Ce CSP prend en charge la dérivation de clés pour les protocoles SSL2, PCT1, SSL3 et TLS1. Le [*hachage*](../secgloss/h-gly.md) se compose d’une concaténation d’un hachage MD5 avec un hachage SHA et signé avec une [*clé privée*](../secgloss/p-gly.md)RSA. Elle peut être exportée vers d’autres pays/régions.



|                   | Valeur                         |
|-------------------|-------------------------------|
| **Type de fournisseur** | PROUVER \_ RSA \_ Schannel           |
| **Nom du fournisseur** | MS \_ Def \_ RSA \_ Schannel \_ Prov  |



 

Pour plus d’informations sur les fournisseurs RSA/Schannel, voir [CSP Functions](cryptography-functions.md).

 

 
