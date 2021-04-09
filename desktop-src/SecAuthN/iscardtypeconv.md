---
description: Fournit les méthodes nécessaires pour prendre en charge les utilisateurs des autres interfaces COM de carte à puce.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interface ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865038"
---
# <a name="iscardtypeconv-interface"></a>Interface ISCardTypeConv

\[L’interface **ISCardTypeConv** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCardTypeConv** fournit les méthodes nécessaires pour prendre en charge les utilisateurs des autres interfaces COM de [*carte à puce*](../secgloss/s-gly.md) . Cette interface n’est fournie qu’à des fins de compatibilité descendante et ne doit plus être utilisée.

## <a name="members"></a>Membres

L’interface **ISCardTypeConv** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardTypeConv** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardTypeConv** possède ces méthodes.



| Méthode                                                                              | Description                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Convertit un tableau d’octets C/C++ classique en une mémoire tampon universelle d’octets (objet **IStream** ).<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Convertit un tableau d’octets mappé dans une mémoire tampon universelle d’octets (objet **IStream** ) en un tableau d’octets C/C++ classique.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Convertit un tableau d’octets mappé dans une mémoire tampon universelle d’octets (objet **IStream** ) en un SafeArray de type non signé (Byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Convertit un tableau d’octets défini en tant que SAFEARRAY en une mémoire tampon universelle d’octets (objet **IStream** ).<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Crée un tableau d’octets.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Crée une mémoire tampon universelle d’octets mappés à un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Crée un SAFEARRAY Automation de caractères non signés (octets).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libère un pointeur de mémoire vers le bloc de mémoire HGLOBAL géré par une interface com **IStream** .<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Acquiert un pointeur d’octet vers le bloc de mémoire HGLOBAL qui est géré par l’interface com **IStream** .<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Détermine la taille (nombre d’octets) d’une interface com **IStream** .<br/>                                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
