---
description: Valeur de la &\# 0034 ; c-hostexe&\# 0034 ; le champ que la source réseau utilise pour la journalisation.
ms.assetid: 82a49719-b9b3-4868-bbcf-9e376f35d4c4
title: MFNETSOURCE_HOSTEXE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6dbde4b4b445e88a0cb6e7ebe45b8b88f386c208854057f209d9c36b7e0024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463649"
---
# <a name="mfnetsource_hostexe-property"></a>MFNETSOURCE \_ propriété HOSTEXE

Valeur du champ « c-hostexe » que la source réseau utilise pour la journalisation. Les applications peuvent définir cette propriété sur le nom de l’application hôte. Par exemple, la valeur peut être « iexplore.exe » si l’application est hébergée dans une page Web.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Chaîne de caractères larges (**WCHAR** \* )

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ HOSTEXE** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Journalisation du client](client-logging.md)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




