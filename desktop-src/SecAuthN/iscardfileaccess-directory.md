---
description: La méthode Directory récupère une liste de fichiers du type spécifié dans le répertoire actif.
ms.assetid: 0ae89811-7534-497b-af9f-ae37a48bc3e5
title: ISCardFileAccess ::D méthode ire
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Directory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 74293d4fa97a61133739cac75f17eaffed6e52b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864049"
---
# <a name="iscardfileaccessdirectory-method"></a>ISCardFileAccess ::D méthode ire

\[La méthode d' **Annuaire** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **Directory** récupère une liste de fichiers du type spécifié dans le répertoire actif.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Directory(
  [in]  FILETYPE    fileType,
  [out] LPSAFEARRAY *ppFileList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*filetype* \[ dans\]
</dt> <dd>

Type de fichiers de [*carte à puce*](../secgloss/s-gly.md) à répertorier.



| Valeur                                                                                                                                                                                      | Signification                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="SC_TYPE_DIRECTORIES"></span><span id="sc_type_directories"></span><dl> <dt>**\_répertoires de type SC \_**</dt> </dl>           | Répertorier uniquement les fichiers du répertoire.<br/>                |
| <span id="SC_TYPE_FILES"></span><span id="sc_type_files"></span><dl> <dt>**\_fichiers de type SC \_**</dt> </dl>                             | Répertorier uniquement les fichiers élémentaires.<br/>               |
| <span id="SC_TYPE_ALL_FILES"></span><span id="sc_type_all_files"></span><dl> <dt>**SC- \_ type \_ tous les \_ fichiers**</dt> </dl>                | Répertoriez à la fois le répertoire et les fichiers élémentaires.<br/> |
| <span id="SC_TYPE_DIRECTORY_FILE"></span><span id="sc_type_directory_file"></span><dl> <dt>**\_fichier de \_ Répertoire de type SC \_**</dt> </dl> | Fichier de répertoire.<br/>                           |
| <span id="SC_TYPE_TRANSPARENT_EF"></span><span id="sc_type_transparent_ef"></span><dl> <dt>**\_type SC \_ transparent \_ EF**</dt> </dl> | Fichier élémentaire transparent.<br/>              |
| <span id="SC_TYPE_FIXED_EF"></span><span id="sc_type_fixed_ef"></span><dl> <dt>**\_type SC \_ fixe \_ EF**</dt> </dl>                   | Fichier élémentaire fixe linéaire.<br/>             |
| <span id="SC_TYPE_CYCLIC_EF"></span><span id="sc_type_cyclic_ef"></span><dl> <dt>**SC \_ type \_ \_ EF cyclique**</dt> </dl>                | Fichier élémentaire cyclique.<br/>                   |
| <span id="SC_TYPE_VARIABLE_EF"></span><span id="sc_type_variable_ef"></span><dl> <dt>**\_variable de type SC \_ \_ EF**</dt> </dl>          | Fichier élémentaire de variable linéaire.<br/>          |



 

</dd> <dt>

*ppFileList* \[ à\]
</dt> <dd>

Tableau de BSTR représentant la liste des fichiers correspondant au spécificateur dans *filetype*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                             |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | L’interface n’a pas implémenté cette méthode.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                                 |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été transmis pour *ppFileList*.<br/>  |



 

## <a name="remarks"></a>Notes

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
</dt> </dl>

 

 
