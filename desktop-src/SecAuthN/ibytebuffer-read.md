---
description: La méthode Read lit un nombre spécifié d’octets à partir de l’objet buffer dans la mémoire en commençant au pointeur de recherche actuel.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer :: Read, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb78726228e333205032a3179e5c3bedb05786b072d02e78d5cc85cea7a97336
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482669"
---
# <a name="ibytebufferread-method"></a>IByteBuffer :: Read, méthode

\[La méthode de **lecture** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]

La méthode **Read** lit un nombre spécifié d’octets à partir de l’objet buffer dans la mémoire en commençant au pointeur de recherche actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pByte* \[ à\]
</dt> <dd>

Pointe vers la mémoire tampon dans laquelle les données de flux sont lues. Si une erreur se produit, cette valeur est **null**.

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Nombre d’octets de données à tenter de lire à partir de l’objet de flux.

</dd> <dt>

*pcbRead* \[ à\]
</dt> <dd>

Adresse d’une variable de **type long** qui reçoit le nombre réel d’octets lus à partir de l’objet de flux. Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur. Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets lus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un **HRESULT**. La valeur S \_ OK indique que l’appel a réussi.

## <a name="remarks"></a>Remarques

Cette méthode lit les octets de cet objet de flux dans la mémoire. L’objet de flux doit être ouvert en \_ mode de lecture STGM. Cette méthode ajuste le pointeur de recherche par le nombre réel d’octets lus.

Le nombre d’octets réellement lus est également retourné dans le paramètre *pcbRead* .

Notes pour les appelants

Le nombre réel d’octets lus peut être inférieur au nombre d’octets demandés si une erreur se produit ou si la fin du flux est atteinte pendant l’opération de lecture.

Certaines implémentations peuvent retourner une erreur si la fin du flux est atteinte pendant la lecture. Vous devez être prêt à gérer les valeurs de retour des erreurs return ou S \_ OK à la fin des lectures de flux.

## <a name="examples"></a>Exemples

L’exemple suivant illustre la lecture d’octets à partir de la mémoire tampon.


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



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



 

