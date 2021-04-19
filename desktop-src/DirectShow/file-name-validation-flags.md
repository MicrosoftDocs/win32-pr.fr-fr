---
description: Ces indicateurs spécifient le comportement du localisateur de média.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Indicateurs de validation du nom de fichier (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528511"
---
# <a name="file-name-validation-flags"></a>Indicateurs de validation du nom de fichier

\[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

Ces indicateurs spécifient le comportement du localisateur de média.



| Constante/valeur                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ \_Vérification VALIDATEF**</dt> <dt>0x01</dt> </dl>                   | Vérifiez la validité des noms de fichiers. Vous devez définir cet indicateur pour valider les noms de fichiers. Si ce n’est pas le cas, les autres indicateurs n’ont aucun effet.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ VALIDATEF \_ Popup**</dt> <dt>0x02</dt> </dl>                   | Si un fichier est introuvable, affichez une boîte de dialogue Ouvrir un fichier pour l’utilisateur final.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Si un fichier manquant est trouvé, affichez brièvement une boîte de message avec le nom et l’emplacement du fichier. Cet indicateur est surtout utile à des fins de test. la boîte de message n’est probablement pas adaptée à un produit de vente au détail.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ VALIDATEF \_ remplace**</dt> <dt>0x08</dt> </dl>             | Si un fichier manquant est trouvé, mettez à jour le nom de l’objet source. (Valide uniquement dans la méthode [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Utilisez toujours un fichier local, même si une version du fichier existe sur le réseau.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt> </dl>                | Ne pas rechercher les fichiers manquants. Les noms de fichiers sont toujours validés si vous définissez l' \_ indicateur de vérification SFN VALIDATEF \_ .<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Ignorer les objets source muets. (Valide uniquement dans la méthode [**IAMTimeline :: ValidateSourceNames**](iamtimeline-validatesourcenames.md) .)<br/>                                                                                |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




