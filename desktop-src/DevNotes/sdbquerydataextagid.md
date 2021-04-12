---
description: Récupère des données à partir des entrées spécifiées appartenant à une entrée EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: SdbQueryDataExTagID fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392939"
---
# <a name="sdbquerydataextagid-function"></a>SdbQueryDataExTagID fonction)

Récupère des données à partir des entrées spécifiées appartenant à une entrée EXE.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

fichier *PDB* \[ dans\]
</dt> <dd>

Handle de la base de données de shims.

</dd> <dt>

*tiExe* \[ dans\]
</dt> <dd>

[**TagId**](tagid.md) de l’entrée exe.

</dd> <dt>

*lpszDataName* \[ dans, facultatif\]
</dt> <dd>

Nom de l’entrée de données à récupérer. Pour spécifier plusieurs entrées, séparez les noms par des barres obliques inverses (« \\ »). Si ce paramètre a la **valeur null**, la fonction tente de retourner toutes les entrées de données.

</dd> <dt>

*lpdwDataType* \[ out, facultatif\]
</dt> <dd>

Type de données des entrées retournées. Ce paramètre peut prendre l’une des valeurs suivantes :

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

**\_fichier binaire reg**
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

**\_valeur DWORD reg**
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

**REG \_ multiple \_ SZ**
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

**REG \_ aucun**
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

**\_q QWord**
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

**SZ de REG \_**
</dt> </dl> </dd> <dt>

*lpBuffer* \[ à\]
</dt> <dd>

Mémoire tampon qui reçoit les données. Si la mémoire tampon n’est pas assez grande pour contenir les données, la fonction échoue et retourne une **\_ \_ mémoire tampon insuffisante**.

</dd> <dt>

*lpcbBufferSize* \[ in, out, facultatif\]
</dt> <dd>

Taille de la mémoire tampon *lpBuffer* , en octets.

</dd> <dt>

*ptiData* \[ à\]
</dt> <dd>

[**TagId**](tagid.md) de l’entrée de données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne l’une des valeurs suivantes.



| Code de retour                                                                                                    | Description                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>       | Un ou plusieurs paramètres d’entrée sont incorrects.<br/>                  |
| <dl> <dt>**ERREUR d’altération de la \_ \_ base de DB interne \_**</dt> </dl> | Aucune entrée de données n’a été trouvée pour l’entrée EXE.<br/>               |
| <dl> <dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt> </dl>     | La mémoire tampon n’est pas assez grande pour contenir les entrées de données.<br/> |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>      | L’allocation de mémoire a échoué.<br/>                               |
| <dl> <dt>**ERREUR \_ \_ introuvable**</dt> </dl>               | Une entrée de données portant le nom *lpszDataName* est introuvable.<br/>    |
| <dl> <dt>**ERREUR de \_ réussite**</dt> </dl>                  | La fonction s’est terminée avec succès.<br/>                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




