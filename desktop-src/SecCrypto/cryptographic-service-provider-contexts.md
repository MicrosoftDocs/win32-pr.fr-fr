---
description: La première fonction CryptoAPI appelée par une application qui utilise une API de chiffrement est la fonction CryptAcquireContext.
ms.assetid: ad1ff45c-7d02-431b-a287-e9db765476ce
title: Contextes de fournisseur de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df20df528b0ba0c385c7ab690436351d918f1521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112683"
---
# <a name="cryptographic-service-provider-contexts"></a>Contextes de fournisseur de services de chiffrement

La première fonction [*CryptoAPI*](../secgloss/c-gly.md) appelée par une application qui utilise une API de chiffrement est la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) . Cette fonction renvoie un descripteur à un CSP particulier qui comprend la spécification d’un [*conteneur de clé*](../secgloss/k-gly.md) particulier au sein du CSP. Ce conteneur de clé est soit un conteneur de clé demandé spécifiquement, soit le conteneur de clé par défaut pour l’utilisateur actuellement connecté.

[**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) peut également créer un conteneur de clé. Pour plus d’informations, consultez [exemple de programme c : création d’un conteneur de clé et génération de clés](example-c-program-creating-a-key-container-and-generating-keys.md) et exemple de [programme c : utilisation de CryptAcquireContext](example-c-program-using-cryptacquirecontext.md).

Un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) a un nom et un type. Par exemple, le nom de l’un des fournisseurs de services de chiffrement actuellement fournis avec le système d’exploitation est [Microsoft base Cryptographic Provider](microsoft-base-cryptographic-provider.md). Il s’agit d’un fournisseur de type [ \_ \_ complet RSA Proven](prov-rsa-full.md) . Le nom de chaque fournisseur est unique ; le type de fournisseur n’est pas.

Lorsqu’une application appelle [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un handle CSP, elle spécifie un type de fournisseur et, éventuellement, un nom de fournisseur. Si un type et un nom sont tous deux spécifiés, la fonction charge le CSP avec le type de fournisseur et le nom de fournisseur correspondants. La fonction retourne le descripteur du CSP qui fournit l’accès à la fois au CSP et à un [*conteneur de clé*](../secgloss/k-gly.md) au sein du CSP.

Lorsqu’une application appelle [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) et spécifie un type de fournisseur, mais aucun nom de fournisseur, la fonction recherche un fournisseur nommé, en vérifiant d’abord une liste de fournisseurs nommés par défaut associés à l’utilisateur connecté et, en cas d’échec, à partir d’une liste de fournisseurs nommés par défaut associés à l’ordinateur. Une fois le nom du fournisseur déterminé, la fonction **CryptAcquireContext** recherche le CSP pour ce fournisseur, la charge et retourne son handle.

Lorsque vous avez fini d’utiliser un descripteur CSP, libérez-le en appelant la fonction [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext) .

 

 
