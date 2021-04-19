---
description: Définit le comportement d’invite du magasin protégé chaque fois qu’il affiche une interface utilisateur.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Structure PST_PROMPTINFO (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532630"
---
# <a name="pst_promptinfo-structure"></a>PROMPTINFO PST ( \_ structure)

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Définit le comportement d’invite du magasin protégé chaque fois qu’il affiche une interface utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

**dwPromptFlags**
</dt> <dd>

Cet indicateur est ignoré.



| Valeur                                                                                                                                                                                                                                          | Signification                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**Fichier PST \_ PF \_ \_ affiche toujours**</dt> <dt>0x00000001</dt> </dl> | Demande que le fournisseur affiche la boîte de dialogue d’invite à l’utilisateur, même s’il n’est pas requis pour cet accès. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**Fichier PST \_ PF \_ ne jamais \_ Afficher**</dt> <dt>0x00000002</dt> </dl>    | N’affiche pas la boîte de dialogue d’invite à l’utilisateur.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

Handle de la fenêtre parente pour l’interface utilisateur. Le membre **hwndApp** détermine l’emplacement où l’interface utilisateur s’affiche. Si la **valeur null** est passée, le bureau est considéré comme la fenêtre parente.

</dd> <dt>

**szPrompt**
</dt> <dd>

Chaîne d’invite.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
