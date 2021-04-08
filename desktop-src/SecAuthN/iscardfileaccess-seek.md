---
description: La méthode Seek sélectionne l’objet à partir duquel l’accès (lecture/écriture) sera effectué.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'ISCardFileAccess :: Seek, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756880"
---
# <a name="iscardfileaccessseek-method"></a>ISCardFileAccess :: Seek, méthode

\[La méthode **Seek** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Seek** sélectionne l’objet à partir duquel l’accès (lecture/écriture) sera effectué.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle du fichier ouvert.

</dd> <dt>

*Recherche* \[ dans\]
</dt> <dd>

Emplacement où la recherche doit commencer.



| Valeur                                                                                                | Signification                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ Seek \_ depuis le \_ début</dt> </dl> | Commencez la recherche au début.<br/>          |
| <dl> <dt>SC \_ Seek \_ à partir de \_ end </dt> </dl>      | Commencer la recherche à partir de la fin.<br/>              |
| <dl> <dt>SC \_ Seek \_ relative</dt> </dl>        | Commence la recherche à partir de la position actuelle.<br/> |



 

</dd> <dt>

*lOffset* \[ dans\]
</dt> <dd>

Nombre d’objets de données de l’objet de référence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

Pour lire ou écrire à partir d’un fichier, appelez [**en lecture ou en**](iscardfileaccess-read.md) [**écriture**](iscardfileaccess-write.md) , respectivement.

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

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
</dt> <dt>

[**En lecture**](iscardfileaccess-read.md)
</dt> <dt>

[**Ecrire**](iscardfileaccess-write.md)
</dt> </dl>

 

 
