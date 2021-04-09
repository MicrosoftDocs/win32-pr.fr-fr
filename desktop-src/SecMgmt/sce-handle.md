---
description: Le \_ type de données du handle SCE est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par \_ les informations de requête PFSCE \_ et \_ \_ les fonctions de prise en charge d’PFSCE Set info pour transmettre des informations entre la pièce jointe et la base de données de sécurité.
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112658"
---
# <a name="sce_handle"></a>\_handle SCE

Le type de données du **\_ handle SCE** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par [**les \_ \_ informations de requête PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) et les fonctions de prise en charge d' [**PFSCE \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) pour transmettre des informations entre la pièce jointe et la base de données de sécurité.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations sur la requête PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**PFSCE \_ définir des \_ informations**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

