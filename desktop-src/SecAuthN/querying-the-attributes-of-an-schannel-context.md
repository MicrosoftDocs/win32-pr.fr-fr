---
description: Fournit des informations spécifiques à Schannel sur un contexte de sécurité.
ms.assetid: 6ff4ebcc-2362-4397-ae77-2d378db8c7e2
title: Interrogation des attributs d’un contexte Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6951aee242b12cc5fcc7f9c52de7e793c2e92733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112167"
---
# <a name="querying-the-attributes-of-an-schannel-context"></a>Interrogation des attributs d’un contexte Schannel

La fonction [**QueryContextAttributes (SChannel)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesw) fournit des informations spécifiques à Schannel sur un [*contexte de sécurité*](../secgloss/s-gly.md). La plupart des informations sont spécifiées à l’origine lors de la création du contexte à l’aide de la fonction client [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou Server [**AcceptSecurityContext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Certaines informations sont spécifiées lors de l’obtention d’un descripteur des informations d’identification utilisées pour créer le contexte. Pour plus d’informations, consultez [obtention d’informations d’identification Schannel](obtaining-schannel-credentials.md).

 

 
