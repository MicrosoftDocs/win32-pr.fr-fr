---
description: Le SSP Schannel implémente les versions des protocoles TLS, DTLS et SSL. Les différentes versions de Windows prennent en charge différentes versions de protocole.
ms.assetid: FF716A4E-ABF2-4773-9588-9D200945A866
title: Protocoles dans TLS/SSL (SSP Schannel)
ms.topic: article
ms.date: 01/20/2021
ms.custom: contperf-fy21q3
ms.openlocfilehash: 844d75230119b747f77697f67ddecec5f64ce7cf
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/17/2021
ms.locfileid: "103953338"
---
# <a name="protocols-in-tlsssl-schannel-ssp"></a>Protocoles dans TLS/SSL (SSP Schannel)

Le SSP Schannel implémente les versions des protocoles TLS, DTLS et SSL. Les différentes versions de Windows prennent en charge différentes versions de protocole.

## <a name="tls-protocol-version-support"></a>Prise en charge des versions de protocole TLS

Le tableau suivant indique la prise en charge par le fournisseur Microsoft Schannel des versions du protocole TLS.

*Conseil : vous devrez peut-être faire défiler horizontalement pour afficher toutes les colonnes de cette table :*

| Système d’exploitation Windows | Client TLS 1,0 | Serveur TLS 1,0 | Client TLS 1,1 | Serveur TLS 1,1 | Client TLS 1,2 | Serveur TLS 1,2 | Client TLS 1,3 | Serveur TLS 1,3 |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Windows Vista/Windows Server 2008                     | activé        | activé        | Non pris en charge  | Non pris en charge  | Non pris en charge  | Non pris en charge  | Non pris en charge  | Non pris en charge  |
| Windows Server 2008 avec Service Pack 2 (SP2)         | activé        | activé        | Désactivé       | Désactivé       | Désactivé       | Désactivé       | Non pris en charge  | Non pris en charge  |
| Windows 7/Windows Server 2008 R2                      | activé        | activé        | Désactivé       | Désactivé       | Désactivé       | Désactivé       | Non pris en charge  | Non pris en charge  |
| Windows 8/Windows Server 2012                         | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 8.1/Windows Server 2012 R2                    | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1507                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1511                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1607/Windows Server 2016 standard | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10 version 1703                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1709                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10 version 1803                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1809                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10 version 1903                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 1909                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  | 
| Windows 10, version 2004                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows 10, version 20H2                              | activé        | activé        | activé        | activé        | activé        | activé        | Non pris en charge  | Non pris en charge  |
| Windows Server 2022                              | activé        | activé        | activé        | activé        | activé        | activé        | activé        | activé        |


## <a name="dtls-protocol-version-support"></a>Prise en charge des versions de protocole DTLS

La liste suivante répertorie la prise en charge par le fournisseur Microsoft Schannel des versions du protocole DTLS.

*Conseil : vous devrez peut-être faire défiler horizontalement pour afficher toutes les colonnes de cette table :*

| Système d’exploitation Windows                                            | Client DTLS 1,0 | Serveur DTLS 1,0 | Client DTLS 1,2 | Serveur DTLS 1,2 |
|-------------------------------------------------------|-----------------|-----------------|-----------------|-----------------|
| Windows Vista/Windows Server 2008                     | Non pris en charge   | Non pris en charge   | Non pris en charge   | Non pris en charge   |
| Windows Server 2008 avec SP2                          | Non pris en charge   | Non pris en charge   | Non pris en charge   | Non pris en charge   |
| Windows 7/Windows Server 2008 R2                      | activé         | activé         | Non pris en charge   | Non pris en charge   |
| Windows 8/Windows Server 2012                         | activé         | activé         | Non pris en charge   | Non pris en charge   |
| Windows 8.1/Windows Server 2012 R2                    | activé         | activé         | Non pris en charge   | Non pris en charge   |
| Windows 10, version 1507                              | activé         | activé         | Non pris en charge   | Non pris en charge   |
| Windows 10, version 1511                              | activé         | activé         | Non pris en charge   | Non pris en charge   |
| Windows 10, version 1607/Windows Server 2016 standard | activé         | activé         | activé         | activé         |
| Windows 10 version 1703                              | activé         | activé         | activé         | activé         |
| Windows 10 version 1803                              | activé         | activé         | activé         | activé         |
| Windows 10, version 1809                              | activé         | activé         | activé         | activé         |
| Windows 10 version 1903                              | activé         | activé         | activé         | activé         |
| Windows 10, version 1909                              | activé         | activé         | activé         | activé         |
| Windows 10, version 2004                              | activé         | activé         | activé         | activé         |
| Windows 10, version 20H2                              | activé         | activé         | activé         | activé         |
| Windows 10, version 21H1                              | activé         | activé         | activé         | activé         |

## <a name="pre-tls-standard-protocols-support"></a>Prise en charge des protocoles standard antérieurs à TLS

La liste suivante répertorie la prise en charge par le fournisseur Microsoft Schannel des protocoles standard antérieurs à TLS :

*Conseil : vous devrez peut-être faire défiler horizontalement pour afficher toutes les colonnes de cette table :*

| Système d’exploitation Windows                                            | PCT 1.0       | Client SSL2   | Serveur SSL2   | Client SSL3 | Serveur SSL3 |
|-------------------------------------------------------|---------------|---------------|---------------|-------------|-------------|
| Windows Vista/Windows Server 2008                     | Non pris en charge | Désactivé      | activé       | activé     | activé     |
| Windows Server 2008 avec SP2                          | Non pris en charge | Désactivé      | activé       | activé     | activé     |
| Windows 7/Windows Server 2008 R2                      | Non pris en charge | Désactivé      | activé       | activé     | activé     |
| Windows 8/Windows Server 2012                         | Non pris en charge | Désactivé      | Désactivé      | activé     | activé     |
| Windows 8.1/Windows Server 2012 R2                    | Non pris en charge | Désactivé      | Désactivé      | activé     | activé     |
| Windows 10, version 1507                              | Non pris en charge | Désactivé      | Désactivé      | activé     | activé     |
| Windows 10, version 1511                              | Non pris en charge | Désactivé      | Désactivé      | activé     | activé     |
| Windows 10, version 1607/Windows Server 2016 standard | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10 version 1703                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10 version 1803                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10, version 1809                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10 version 1903                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10, version 1909                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10, version 2004                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10, version 20H2                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |
| Windows 10, version 20H1                              | Non pris en charge | Non pris en charge | Non pris en charge | Désactivé    | Désactivé    |


> [!IMPORTANT]
> À partir de Windows 10, version 1607 et Windows Server 2016, SSL 2,0 a été supprimé et n’est plus pris en charge.

> [!TIP]  
> Toutes les versions de Windows acceptent un message au format unifié « ClientHello », même si SSL version 2 est désactivé ou n’est plus pris en charge.
