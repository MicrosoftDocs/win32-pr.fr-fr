---
description: La méthode Write écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer :: Write, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096406"
---
# <a name="ibytebufferwrite-method"></a>IByteBuffer :: Write, méthode

\[La méthode **Write** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Write** écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pByte* \[ dans\]
</dt> <dd>

Adresse de la mémoire tampon contenant les données à écrire dans le flux. Un pointeur valide doit être fourni pour ce paramètre même quand *CB* est égal à zéro.

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Nombre d’octets de données à tenter d’écrire dans le flux. Ce paramètre peut être égal à zéro.

</dd> <dt>

*pcbWritten* \[ à\]
</dt> <dd>

Adresse d’une variable de **type long** où cette méthode écrit le nombre réel d’octets écrits dans l’objet de flux. L’appelant peut affecter la **valeur null** à ce pointeur, auquel cas cette méthode ne fournit pas le nombre réel d’octets écrits.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Notes

La méthode **IByteBuffer :: Write** écrit les données spécifiées dans un objet de flux. Le pointeur de recherche est ajusté pour le nombre d’octets réellement écrits. Le nombre d’octets réellement écrits est retourné dans le paramètre *pcbWritten* . Si le nombre d’octets est de zéro octet, l’opération d’écriture n’a aucun effet.

Si le pointeur de recherche se trouve actuellement au-delà de la fin du flux et que le nombre d’octets est différent de zéro, cette méthode augmente la taille du flux au pointeur de recherche et écrit les octets spécifiés à partir du pointeur de recherche. Les octets de remplissage écrits dans le flux de données ne sont pas initialisés à une valeur particulière. Il s’agit du même comportement que celui de la fin du fichier dans le système de fichiers FAT MS-DOS.

Avec un nombre zéro octet et un pointeur de recherche au-delà de la fin du flux, cette méthode ne crée pas les octets de remplissage pour augmenter le flux vers le pointeur de recherche. Dans ce cas, vous devez appeler la méthode [**IByteBuffer :: assets**](ibytebuffer-setsize.md) pour augmenter la taille du flux et écrire les octets de remplissage.

Le paramètre *pcbWritten* peut avoir une valeur même si une erreur se produit.

Dans l’implémentation fournie par COM, les objets de flux ne sont pas éparpillés. Tout octet de remplissage est finalement alloué sur le disque et affecté au flux.

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’écriture d’octets dans l’objet de flux.


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a>Spécifications



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



 

