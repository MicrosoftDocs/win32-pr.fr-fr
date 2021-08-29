---
description: Construit une unité de données de protocole d’application de commande valide pour la transmission vers une carte à puce.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'ISCardCmd :: BuildCmd, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aec07516a44dc06489a627c690ec15dd2e0a80edef9fee49801c0ed23d64439f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015259"
---
# <a name="iscardcmdbuildcmd-method"></a>ISCardCmd :: BuildCmd, méthode

\[La méthode **BuildCmd** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **BuildCmd** construit une [*unité de données de protocole d’application*](../secgloss/a-gly.md) de commande valide pour la transmission vers une [*carte à puce*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byClassId* \[ dans\]
</dt> <dd>

Identificateur de classe de commande.

</dd> <dt>

*byInsId* \[ dans\]
</dt> <dd>

Identificateur d’instruction de commande.

</dd> <dt>

*byP1* \[ dans\]
</dt> <dd>

Premier paramètre de la commande.

</dd> <dt>

*byP2* \[ dans\]
</dt> <dd>

Deuxième paramètre de la commande.

</dd> <dt>

*pbyData* \[ dans\]
</dt> <dd>

Pointeur vers la partie données de la commande.

</dd> <dt>

*p1Le* \[ dans\]
</dt> <dd>

Pointeur vers un entier LONG contenant la longueur attendue des données retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | L’un des paramètres n’est pas valide.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>        |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                      |



 

## <a name="remarks"></a>Remarques

Pour encapsuler la commande dans une autre commande, appelez [**encapsuler**](iscardcmd-encapsulate.md).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment construire une commande APDU. L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) et que pIByteRequest est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) initialisée avec un appel précédent à la méthode [**IByteBuffer :: Initialize**](ibytebuffer-initialize.md) .


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Encapsuler**](iscardcmd-encapsulate.md)
</dt> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
