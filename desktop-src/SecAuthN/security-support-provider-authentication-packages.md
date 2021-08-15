---
description: le système d’exploitation Windows prend en charge l’authentification à l’aide de packages de sécurité qui fonctionnent comme des fournisseurs de support de sécurité et comme des packages d’authentification.
ms.assetid: f40060be-fad2-4008-b981-727199d71581
title: Fournisseur de support de sécurité/packages d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62f634d0571eab43652485f8ca1313f78fd157ca202d5d78369552db648de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918338"
---
# <a name="security-support-providerauthentication-packages"></a>Fournisseur de support de sécurité/packages d’authentification

le système d’exploitation Windows prend en charge l’authentification à l’aide de [*packages de sécurité*](../secgloss/s-gly.md) qui fonctionnent comme des fournisseurs de [*support de sécurité*](../secgloss/s-gly.md) et comme des [*packages d’authentification*](../secgloss/a-gly.md). les packages de sécurité fournissent les services de prise en charge du processus d’ouverture de session d’un package d’authentification Windows et fournissent également des services d’authentification aux applications en implémentant un ensemble de fonctions mappées à l’Interface SSPI ( [Security support Provider Interface](sspi.md) ).

Un package de sécurité qui fonctionne comme un package d’authentification et implémente les fonctionnalités requises par l' [*interface SSPI*](../secgloss/s-gly.md) est appelé fournisseur de support de sécurité/package d’authentification (SSP/AP).

Pour plus d’informations sur les packages de sécurité, consultez [packages SSP fournis par Microsoft](ssp-packages-provided-by-microsoft.md). Pour plus d’informations sur le développement d’un fournisseur SSP/APs personnalisé, consultez [packages de sécurité personnalisés](custom-security-packages.md).

 

 
