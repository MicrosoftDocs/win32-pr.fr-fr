---
description: Fournit l’accès au contexte d’un objet de chaîne CAPICOM. Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interface IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a3ac2f2234c986c9a86073e25e1277fa1af4f10f2809e013bc65849120b90c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005437"
---
# <a name="ichaincontext-interface"></a>Interface IChainContext

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

L’interface **IChainContext** fournit l’accès au contexte d’un objet de [**chaîne**](chain.md) CAPICOM. Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette interface lorsque vous devez utiliser un objet de [**chaîne**](chain.md) CAPICOM dans une autre dérivation de CryptoAPI.

## <a name="members"></a>Membres

L’interface **IChainContext** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IChainContext** possède ces méthodes.



| Méthode                                           | Description                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](ichaincontext-freecontext.md) | Libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IChainContext** possède les propriétés suivantes.



| Propriété                                                      | Type d’accès           | Description                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [**ChainContext**](ichaincontext-chaincontext.md)<br/> | Lecture/écriture<br/> | Définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




