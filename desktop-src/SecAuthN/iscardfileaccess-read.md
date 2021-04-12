---
description: La méthode Read lit et retourne les données spécifiées à partir d’un fichier donné.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'ISCardFileAccess :: Read, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203051"
---
# <a name="iscardfileaccessread-method"></a>ISCardFileAccess :: Read, méthode

\[La méthode de **lecture** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Read** lit et retourne les données spécifiées à partir d’un fichier donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle du fichier ouvert auquel accéder.

</dd> <dt>

*lBytesToRead* \[ dans\]
</dt> <dd>

Longueur des données à lire (en) ou nombre d’octets lus (out). Retourne la liste des fichiers sous la forme d’un tableau de BSTR.

</dd> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Spécifie si la messagerie sécurisée doit être utilisée.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ messagerie sécurisée SC FL \_**
</dt> </dl> </dd> <dt>

*ppBuffer* \[ à\]
</dt> <dd>

Objet [**IByteBuffer**](ibytebuffer.md) contenant les données lues.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
