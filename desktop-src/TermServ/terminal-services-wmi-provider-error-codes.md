---
title: Codes d’erreur du fournisseur WMI Services Bureau à distance (Wbemcli. h)
description: Erreurs retournées par le fournisseur WMI Services Bureau à distance. Pour obtenir la liste des autres erreurs WMI, consultez constantes d’erreur WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509382"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Codes d’erreur du fournisseur WMI Services Bureau à distance

La liste suivante répertorie les erreurs WMI retournées par le fournisseur WMI Services Bureau à distance. Pour obtenir la liste des autres erreurs WMI, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**échec de WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Échec de l'appel de la méthode.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



L'objet est introuvable.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_échec du \_ fournisseur WBEM E \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



Le fournisseur a échoué à un moment autre que pendant l’initialisation.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilité de \_ type WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Une incompatibilité de type s’est produite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**\_mémoire WBEM \_ insuffisante \_ \_**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Il n'y a pas assez de mémoire pour l'opération.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**\_paramètre WBEM E \_ non valide \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Un des paramètres de l'appel n'est pas correct.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ non \_ disponible**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



La ressource, généralement un serveur distant, n'est pas disponible actuellement.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



La fonctionnalité ou l'opération n'est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ espace de noms non valide \_**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



L'espace de noms spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ objet non valide \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



L'instance spécifiée n'est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ échec d’initialisation d’E WBEM \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Un module, tel qu’un fournisseur, n’a pas pu s’initialiser pour des raisons internes.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ opération non valide WBEM E \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



L'opération demandée n'est pas valide. Cette erreur s'applique généralement aux tentatives non valides de suppression de classes ou de propriétés. Cette erreur est retournée lors d’une tentative de modification d’une propriété de substitution de serveur par le biais du contrôle de stratégie de groupe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_requête E \_ non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La syntaxe de la requête n'est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_type de \_ requête non valide WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Le langage de la requête demandé n'est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



Dans une opération Put, l’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_syntaxe WBEM E \_ non valide \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La syntaxe de la requête n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_ \_ lecture seule WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



La propriété que vous avez tenté de modifier est en lecture seule.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_fournisseur E \_ WBEM \_ non \_ conforme**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Le fournisseur ne peut pas effectuer l’opération demandée. L’opération peut inclure une requête qui est trop complexe, la récupération d’une instance, la création d’une classe, la mise à jour d’une classe, la suppression d’une classe ou l’énumération d’une classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non conforme \_**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



La valeur **Nothing** / **null** a été spécifiée pour une propriété qui ne peut pas être / **null**, telle que celle qui est marquée par un qualificateur [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**indexé**](/windows/desktop/WmiSdk/optional-qualifiers)ou [**not \_ null**](/windows/desktop/WmiSdk/optional-qualifiers) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valeur WBEM \_ E \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La demande a été effectuée avec une valeur hors limites ou est incompatible avec le type.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ , \_ méthode non valide**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



La méthode demandée n'est pas disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_paramètres de méthode WBEM E \_ non valides \_ \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Les paramètres fournis pour la méthode ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ \_ chemin d’objet non valide \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Le chemin d’accès à l’objet spécifié n’est pas valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



 

