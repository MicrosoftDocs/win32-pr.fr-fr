---
description: Spécification des chiffrements Schannel et des forces de chiffrement
ms.assetid: b87d3e72-df7b-4a00-854e-c3706565ed7d
title: Spécification des chiffrements Schannel et des forces de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04ec37cfea633814881fba5bfd71ad15205a1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524370"
---
# <a name="specifying-schannel-ciphers-and-cipher-strengths"></a>Spécification des chiffrements Schannel et des forces de chiffrement

Pour les échanges d’informations client/serveur, le comportement par défaut de Schannel est de négocier le meilleur chiffrement disponible en fonction de ceux qui sont activés dans le registre. Les applications peuvent limiter les chiffrements et les niveaux de chiffrement autorisés pour une connexion à l’aide des membres de la structure [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) , comme suit :

1.  Définissez le membre **palgSupportedAlgs** sur un tableau d' [**\_ ID ALG**](../seccrypto/alg-id.md) contenant les chiffrements autorisés. Pour plus d’informations, consultez chiffrement des ID.
2.  Définissez les membres **dwMinimumCipherStrength** et/ou **dwMaximumCipherStrength** sur les forces minimales et maximales autorisées. Pour plus d’informations, consultez valeurs de niveau de chiffrement.
3.  Transmettez la structure [**Schannel \_ cred**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (au moyen du paramètre *pAuthData* ) dans un appel à la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) . Cette fonction retourne un handle d’informations d’identification.
4.  Spécifiez le descripteur des informations d’identification dans un appel à la fonction [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) côté client ou à la fonction [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) côté serveur.

## <a name="cipher-ids"></a>ID de chiffrement

Le comportement par défaut de Schannel consiste à demander le chiffrement le mieux disponible en fonction des entrées Schannel dans le registre système. Ne modifiez pas le registre système. les paramètres qu’il contient pour Schannel sont utilisés globalement et affectent les autres applications. Pour obtenir la liste des constantes valides, consultez [**ALG \_ ID**](../seccrypto/alg-id.md).

## <a name="cipher-strength-values"></a>Valeurs de niveau de chiffrement

Cette fonctionnalité Schannel est généralement utilisée pour limiter une connexion à des chiffrements de niveau national ou d’exportation. Les forces nationales incluent 56 et 128 bits, tandis que la puissance d’exportation est limitée à 56 bits. Si vous définissez les valeurs minimale et maximale sur zéro, Schannel utilise tous les niveaux de chiffrement disponibles.

À l’aide de TLS ou SSL 3,0, définissez le membre **dwMinimumCipherStrength** sur-1 (moins un) pour activer les suites de chiffrement « chiffrement NULL », qui fournissent des signatures, mais pas de chiffrement. Si **dwMaximumCipherStrength** a également la valeur-1, seules les suites « chiffrement NULL » seront activées. Ce paramètre est destiné uniquement au développement et ne doit pas être utilisé dans les systèmes de production.

## <a name="querying-cipher-information"></a>Interrogation des informations de chiffrement

Pour récupérer les paramètres de niveau de chiffrement pour les informations d’identification, appelez la fonction [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) et spécifiez les \_ forces de chiffrement SECPKG attr \_ \_ comme paramètre *ulAttribute* .

Pour récupérer la liste des algorithmes pris en charge pour les informations d’identification, appelez [**QueryCredentialsAttributes**](/windows/desktop/api/Sspi/nf-sspi-querycredentialsattributesa) avec SECPKG \_ attr \_ pris en charge \_ algs comme paramètre *ulAttribute* .

 

 
