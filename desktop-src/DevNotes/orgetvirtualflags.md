---
description: Récupère les indicateurs virtuels sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 2a04c257-e3b0-415b-97d2-616e12513a0a
title: ORGetVirtualFlags, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 8f0e44c388b576bb514ed86f2a537cefaf1a4f0984e3e5beb1b466e88c5b82c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076053"
---
# <a name="orgetvirtualflags-function"></a>ORGetVirtualFlags fonction)

Récupère les indicateurs virtuels sur la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORGetVirtualFlags(
  _In_  ORHKEY Handle,
  _Out_ PDWORD pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*pdwFlags* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit les indicateurs de virtualisation définis pour la clé. Une fois que la fonction a retourné une valeur, ce paramètre peut avoir une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <dt>**Reg \_ La clé ne dispose pas d’un \_ \_ \_ échec silencieux**</dt> <dt>4</dt> </dl> | Si cet indicateur est défini et qu’une opération d’ouverture échoue sur une clé pour laquelle la virtualisation est activée, le registre ne tente pas de rouvrir la clé. Si cet indicateur est désactivé, le registre tente de rouvrir la clé avec un \_ accès maximal autorisé.<br/>                                                                                            |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <dt>**Reg \_ CLÉ \_ non \_ virtualisée**</dt> <dt>2</dt> </dl>     | Si cet indicateur est défini et qu’une opération de création de clé échoue parce que l’appelant n’a pas le \_ droit créer une \_ sous- \_ clé de clé sur la clé parente, le registre fait échouer l’opération de création. Si cet indicateur est désactivé, le registre tente de créer la clé dans le magasin virtuel. L’appelant doit disposer de la clé \_ Read Right sur la clé parente.<br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <dt>**Reg \_ \_ \_ Indicateur recurse de clé**</dt> <dt>8</dt> </dl>              | Si cet indicateur est défini, les indicateurs de virtualisation du Registre sont propagés à partir de la clé parente. Si cet indicateur est désactivé, les indicateurs de virtualisation du registre ne sont pas propagés.<br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="remarks"></a>Remarques

La virtualisation du Registre est une technologie de compatibilité des applications temporaire qui permet d’effectuer des opérations d’écriture dans le Registre qui ont un impact global sur les emplacements par utilisateur. Cette redirection est transparente pour les applications qui lisent ou écrivent dans le registre.

la virtualisation du registre est prise en charge à partir de Windows Vista. toutefois, Microsoft envisage de la supprimer des versions futures du système d’exploitation Windows à mesure que d’autres applications sont compatibles avec Windows Vista. Par conséquent, les applications ne doivent pas dépendre du comportement de la virtualisation du Registre dans le système.

La virtualisation du Registre est activée uniquement pour les éléments suivants :

-   processus interactifs 32 bits
-   Clés dans **HKEY \_ local \_ machine \\ Software**
-   Clés dans lesquelles un administrateur peut écrire

Pour plus d’informations, consultez [virtualisation du Registre](../sysinfo/registry-virtualization.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORSetVirtualFlags**](orsetvirtualflags.md)
</dt> <dt>

[Virtualisation du Registre](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
