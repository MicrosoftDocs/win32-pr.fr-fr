---
description: Fournit l’accès au contexte d’un objet de certificat CAPICOM X. 509v3. Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Interface ICertContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 693e259c730209049f669d1499001d026b3d11088c7bef09616826a4673cac0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006037"
---
# <a name="icertcontext-interface"></a>Interface ICertContext

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

L’interface **ICertContext** fournit l’accès au contexte d’un objet de [**certificat**](certificate.md) CAPICOM X. 509v3. Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette interface lorsque vous devez utiliser un objet de [**certificat**](certificate.md) CAPICOM dans une autre dérivation de CryptoAPI.

## <a name="members"></a>Membres

L’interface **ICertContext** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ICertContext** possède ces méthodes.



| Méthode                                          | Description                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**FreeContext**](icertcontext-freecontext.md) | Libère un \_ contexte PCCERT acquis par le biais de la propriété [**CertContext**](icertcontext-certcontext.md) .<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **ICertContext** possède les propriétés suivantes.



| Propriété                                                   | Type d’accès           | Description                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**CertContext**](icertcontext-certcontext.md)<br/> | Lecture/écriture<br/> | Définit ou récupère le contexte PCCERT \_ d’un certificat.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




