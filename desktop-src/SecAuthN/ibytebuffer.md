---
description: L’interface IByteBuffer est fournie pour lire, écrire et gérer les objets de flux. Cet objet est essentiellement un wrapper pour l’objet IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interface IByteBuffer (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8f0aa81106629142efeec7e22bdb495bea853c3c689d6b55887a62f896d89d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417409"
---
# <a name="ibytebuffer-interface"></a>Interface IByteBuffer

\[L’interface **IByteBuffer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

L’interface **IByteBuffer** est fournie pour lire, écrire et gérer les objets de flux. Cet objet est essentiellement un wrapper pour l’objet **IStream** .

## <a name="members"></a>Membres

L’interface **IByteBuffer** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IByteBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IByteBuffer** possède ces méthodes.



| Méthode                                           | Description                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Répliqué**](ibytebuffer-clone.md)               | Clone un objet **IByteBuffer** .<br/>                                                              |
| [**Commiter**](ibytebuffer-commit.md)             | Valide une [*transaction*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copie les octets dans un autre objet.<br/>                                                                |
| [**Initialiser**](ibytebuffer-initialize.md)     | Initialise l’objet **IByteBuffer** .<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Restreint l’accès à une plage d’octets.<br/>                                                          |
| [**Lire**](ibytebuffer-read.md)                 | Lit les octets dans la mémoire.<br/>                                                                       |
| [**Rétablir**](ibytebuffer-revert.md)             | Ignore les modifications apportées depuis le dernier appel de [**validation**](ibytebuffer-commit.md) .<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Modifie le pointeur de recherche.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Modifie la taille de l'objet de flux.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Récupère des informations statistiques sur un flux.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Supprime la restriction d’accès précédemment définie par [**LockRegion**](ibytebuffer-lockregion.md).<br/>     |
| [**Écriture**](ibytebuffer-write.md)               | Écrit des octets dans le flux.<br/>                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

