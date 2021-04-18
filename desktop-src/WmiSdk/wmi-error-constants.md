---
description: Si une erreur se produit, WMI retourne un code d’erreur sous la forme d’une valeur HRESULT. Ces codes peuvent être renvoyés par des scripts, des applications C++ ou WMIC.
ms.assetid: b560f37c-da22-4745-8d1f-b27afdf572ec
ms.tgt_platform: multiple
title: Constantes d’erreur WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95db7220bdc9669716dbe19f5bf2f4e139dfe5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519816"
---
# <a name="wmi-error-constants"></a>Constantes d’erreur WMI

Si une erreur se produit, WMI retourne un code d’erreur sous la forme d’une valeur **HRESULT** . Ces codes peuvent être renvoyés par des scripts, des applications C++ ou [**WMIC**](wmic.md).

> [!Note]
>
> La documentation suivante est destinée aux développeurs et aux administrateurs informatiques. Si vous êtes un utilisateur final qui a rencontré un message d’erreur concernant WMI, vous devez accéder à [support Microsoft](https://support.microsoft.com/) et rechercher le code d’erreur que vous voyez dans le message d’erreur. Pour plus d’informations sur la résolution des problèmes liés aux scripts WMI et au service WMI, consultez [WMI ne fonctionne pas](/previous-versions/tn-archive/ff406382(v=msdn.10)).
>
> Si WMI renvoie des messages d’erreur, sachez qu’ils ne peuvent pas indiquer des problèmes dans le service WMI ou les fournisseurs WMI. Les échecs peuvent provenir d’autres parties du système d’exploitation et émerger comme des erreurs via WMI. Dans tous les cas, ne supprimez pas le référentiel WMI en tant que première action, car la suppression du dépôt peut endommager le système ou les applications installées.
>
> Pour obtenir plus d’informations sur la source du problème, vous pouvez télécharger et exécuter l’outil en ligne de commande [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic. Cet outil génère un rapport qui peut généralement isoler la source du problème et fournir des instructions sur la façon de le résoudre. Le rapport aide également les services de support technique Microsoft à vous aider. Vous pouvez télécharger les WMI Diagnosis Utility [ici](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).

 

Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple). Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes. Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible.

La liste suivante répertorie certaines plages d’erreurs courantes.

<dl> <dt>

<span id="0x80041068_-_0x80041099"></span><span id="0X80041068_-_0X80041099"></span>0x80041068 - 0x80041099
</dt> <dd>

Erreurs qui proviennent de WMI lui-même.

Une opération WMI spécifique a échoué en raison de

-   Une erreur dans la requête, par exemple, une requête WQL échoue ou le compte ne dispose pas des autorisations appropriées.
-   Un problème d’infrastructure WMI, tel qu’une inscription CIM ou DCOM incorrecte.

</dd> <dt>

<span id="0x8007xxxx"></span><span id="0X8007XXXX"></span>0x8007xxxx
</dt> <dd>

Erreurs provenant du système d’exploitation principal. WMI peut renvoyer ce type d’erreur en raison d’une défaillance externe, par exemple, une défaillance de sécurité DCOM.

</dd> <dt>

<span id="0x80040xxx"></span><span id="0X80040XXX"></span>0x80040xxx
</dt> <dd>

Erreurs provenant de DCOM. Par exemple, la configuration DCOM pour les opérations sur un ordinateur distant est peut-être incorrecte.

</dd> <dt>

<span id="0x8005xxxx"></span><span id="0X8005XXXX"></span>0x8005xxxx
</dt> <dd>

Erreur provenant d’ADSI (Active Directory Service Interfaces) ou LDAP (Lightweight Directory Access Protocol), par exemple, un échec d’accès Active Directory lors de l’utilisation des fournisseurs de Active Directory WMI.

</dd> </dl>

Certaines méthodes des classes WMI peuvent retourner des codes d’erreur système et réseau (64, par exemple). Vous pouvez vérifier la définition de ces types de codes d’erreur à l’aide de la commande **net helpmsg** dans la fenêtre d’invite de commandes. Par exemple, la commande **net helpmsg 64** retourne le message : le nom réseau spécifié n’est plus disponible. En C++, vous pouvez appeler [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) et spécifier le module de message **C : \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** .

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**échec de WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Échec de l’appel.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



L’objet est introuvable.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ACCESS_DENIED"></span><span id="wbem_e_access_denied"></span>**\_accès WBEM \_ E \_ refusé**
</dt> <dd> <dl> <dt>

2147749891 (0x80041003)
</dt> <dt>



L’utilisateur actuel n’est pas autorisé à effectuer l’action.


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



Mémoire insuffisante pour l’opération.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CONTEXT"></span><span id="wbem_e_invalid_context"></span>**\_ \_ contexte non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749895 (0x80041007)
</dt> <dt>



L’objet [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) n’est pas valide.


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



La ressource, généralement un serveur distant, n’est pas disponible actuellement.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CRITICAL_ERROR"></span><span id="wbem_e_critical_error"></span>**\_erreur WBEM E \_ critique \_**
</dt> <dd> <dl> <dt>

2147749898 (0x8004100A)
</dt> <dt>



Une erreur interne, critique et inattendue s’est produite. Signalez l’erreur au support technique Microsoft.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_STREAM"></span><span id="wbem_e_invalid_stream"></span>**\_ \_ flux non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749899 (0x8004100B)
</dt> <dt>



Un ou plusieurs paquets de réseau ont été endommagés pendant une session distante.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**WBEM \_ E \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



La fonctionnalité ou l’opération n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SUPERCLASS"></span><span id="wbem_e_invalid_superclass"></span>**la \_ \_ superclasse WBEM E non valide \_**
</dt> <dd> <dl> <dt>

2147749901 (0x8004100D)
</dt> <dt>



La classe parente spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ espace de noms non valide \_**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



L’espace de noms spécifié est introuvable.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**WBEM \_ E \_ objet non valide \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



L’instance spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CLASS"></span><span id="wbem_e_invalid_class"></span>**WBEM \_ - \_ classe non valide \_**
</dt> <dd> <dl> <dt>

2147749904 (0x80041010)
</dt> <dt>



La classe spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_FOUND"></span><span id="wbem_e_provider_not_found"></span>**\_fournisseur WBEM \_ E \_ \_ introuvable**
</dt> <dd> <dl> <dt>

2147749905 (0x80041011)
</dt> <dt>



Le fournisseur référencé dans le schéma n’a pas d’inscription correspondante.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROVIDER_REGISTRATION"></span><span id="wbem_e_invalid_provider_registration"></span>**\_inscription du \_ fournisseur non valide pour \_ WBEM \_**
</dt> <dd> <dl> <dt>

2147749906
</dt> <dt>



Le fournisseur référencé dans le schéma a une inscription incorrecte ou incomplète.

Cette erreur peut être due à de nombreuses conditions, y compris les suivantes :

-   Commande de l' [ \# espace de noms pragma](pragma-namespace.md) manquante dans le fichier format MOF (MOF) utilisé pour inscrire le fournisseur. Le fournisseur peut être inscrit dans un espace de noms WMI incorrect.
-   Impossible de récupérer l’inscription COM.
-   Le modèle d’hébergement n’est pas valide. Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).
-   Une classe spécifiée dans l’inscription n’est pas valide.
-   Impossible de créer une instance de ou d’hériter de la classe [**\_ \_ Win32Provider**](--win32provider.md) pour créer l’inscription du fournisseur dans le fichier MOF.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_LOAD_FAILURE"></span><span id="wbem_e_provider_load_failure"></span>**\_échec de \_ chargement du fournisseur WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749907 (0x80041013)
</dt> <dt>



COM ne peut pas localiser un fournisseur référencé dans le schéma.

Cette erreur peut être due à de nombreuses conditions, y compris les suivantes :

-   Le fournisseur utilise une DLL WMI qui ne correspond pas au fichier. lib utilisé lors de la génération du fournisseur.
-   La DLL du fournisseur, ou l’une des dll dont elle dépend, est endommagée.
-   Le fournisseur n’a pas pu exporter [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).
-   Le fournisseur in-process n’a pas été inscrit à l’aide de la commande **regsvr32** .
-   Le fournisseur out-of-process n’a pas été inscrit à l’aide du commutateur **/regserver** . Par exemple, **myprog.exe/regserver**.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ échec d’initialisation d’E WBEM \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Échec de l’initialisation d’un composant, tel qu’un fournisseur, pour des raisons internes.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSPORT_FAILURE"></span><span id="wbem_e_transport_failure"></span>**\_échec du \_ transport \_ WBEM**
</dt> <dd> <dl> <dt>

2147749909 (0x80041015)
</dt> <dt>



Une erreur réseau qui empêche un fonctionnement normal s’est produite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**\_ \_ opération non valide WBEM E \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



L’opération demandée n’est pas valide. Cette erreur s'applique généralement aux tentatives non valides de suppression de classes ou de propriétés.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**\_requête E \_ non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



La syntaxe de la requête n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_type de \_ requête non valide WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



Le langage de requête demandé n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**WBEM \_ E \_ \_ existe déjà**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



Dans une opération Put, l’indicateur **wbemChangeFlagCreateOnly** a été spécifié, mais l’instance existe déjà.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_override_not_allowed"></span>**le \_ \_ remplacement WBEM E \_ n’est pas \_ autorisé**
</dt> <dd> <dl> <dt>

2147749914 (0x8004101A)
</dt> <dt>



Impossible d’effectuer l’opération d’ajout sur ce qualificateur, car l’objet propriétaire n’autorise pas les remplacements.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_QUALIFIER"></span><span id="wbem_e_propagated_qualifier"></span>**\_ \_ qualificateur PROPAGÉ E WBEM \_**
</dt> <dd> <dl> <dt>

2147749915 (0x8004101B)
</dt> <dt>



L’utilisateur a tenté de supprimer un qualificateur qui n’était pas détenu. Le qualificateur est hérité d'une classe parente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_PROPERTY"></span><span id="wbem_e_propagated_property"></span>**\_ \_ propriété propagé E de \_ WBEM**
</dt> <dd> <dl> <dt>

2147749916 (0x8004101C)
</dt> <dt>



L’utilisateur a tenté de supprimer une propriété qui n’était pas propriétaire. La propriété est héritée d'une classe parente.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNEXPECTED"></span><span id="wbem_e_unexpected"></span>**WBEM \_ E \_ inattendu**
</dt> <dd> <dl> <dt>

2147749917 (0x8004101D)
</dt> <dt>



Le client a effectué une séquence d’appels inattendue et non conforme, telle que l’appel de [**EndEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-endenumeration) avant d’appeler [**BeginEnumeration**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-beginenumeration).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_OPERATION"></span><span id="wbem_e_illegal_operation"></span>**\_ \_ opération non conforme WBEM E \_**
</dt> <dd> <dl> <dt>

2147749918 (0x8004101E)
</dt> <dt>



L’utilisateur a demandé une opération non conforme, telle que la génération d’une classe à partir d’une instance.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_KEY"></span><span id="wbem_e_cannot_be_key"></span>**WBEM \_ E \_ ne peut pas \_ être une \_ clé**
</dt> <dd> <dl> <dt>

2147749919 (0x8004101F)
</dt> <dt>



Tentative non autorisée de spécifier un qualificateur de clé sur une propriété qui ne peut pas être une clé. Les clés sont spécifiées dans la définition de classe pour un objet et ne peuvent pas être modifiées au niveau de l'instance.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INCOMPLETE_CLASS"></span><span id="wbem_e_incomplete_class"></span>**\_ \_ classe incomplète WBEM E \_**
</dt> <dd> <dl> <dt>

2147749920 (0x80041020)
</dt> <dt>



L’objet actuel n’est pas une définition de classe valide. Soit il est incomplet, soit il n’a pas été inscrit auprès de WMI à l’aide de [**SWbemObject. put \_**](swbemobject-put-.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**\_syntaxe WBEM E \_ non valide \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



La syntaxe de la requête n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONDECORATED_OBJECT"></span><span id="wbem_e_nondecorated_object"></span>**\_objet non \_ décoré WBEM \_**
</dt> <dd> <dl> <dt>

2147749922 (0x80041022)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**\_ \_ lecture seule WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



Une tentative de modification d’une propriété en lecture seule a été effectuée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_fournisseur E \_ WBEM \_ non \_ conforme**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



Le fournisseur ne peut pas effectuer l’opération demandée. Il peut s’agir d’une requête trop complexe, de l’extraction d’une instance, de la création ou de la mise à jour d’une classe, de la suppression d’une classe ou de l’énumération d’une classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_CHILDREN"></span><span id="wbem_e_class_has_children"></span>**la \_ classe WBEM E \_ \_ a des \_ enfants**
</dt> <dd> <dl> <dt>

2147749925 (0x80041025)
</dt> <dt>



Une tentative a été effectuée pour apporter une modification qui invalide une sous-classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_HAS_INSTANCES"></span><span id="wbem_e_class_has_instances"></span>**la \_ classe WBEM E \_ \_ a des \_ instances**
</dt> <dd> <dl> <dt>

2147749926 (0x80041026)
</dt> <dt>



Une tentative de suppression ou de modification d’une classe qui a des instances a été effectuée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUERY_NOT_IMPLEMENTED"></span><span id="wbem_e_query_not_implemented"></span>**\_requête E \_ WBEM \_ non \_ implémentée**
</dt> <dd> <dl> <dt>

2147749927 (0x80041027)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ null non conforme \_**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



La valeur Nothing/**null** a été spécifiée pour une propriété qui doit avoir une valeur, telle que celle qui est marquée par un qualificateur [**Key**](key-qualifier.md), [**indexé**](optional-qualifiers.md)ou **not \_ null** .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER_TYPE"></span><span id="wbem_e_invalid_qualifier_type"></span>**\_type de \_ qualificateur non valide WBEM \_ \_**
</dt> <dd> <dl> <dt>

2147749929 (0x80041029)
</dt> <dt>



Une valeur de variante pour un qualificateur a été fournie qui n’est pas un type de qualificateur légal.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY_TYPE"></span><span id="wbem_e_invalid_property_type"></span>**\_type de \_ propriété non valide WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749930 (0x8004102A)
</dt> <dt>



Le type CIM spécifié pour une propriété n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**\_valeur WBEM \_ E \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



La demande a été effectuée avec une valeur hors limites ou n’est pas compatible avec le type.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_SINGLETON"></span><span id="wbem_e_cannot_be_singleton"></span>**WBEM \_ E \_ ne peut pas \_ être \_ Singleton**
</dt> <dd> <dl> <dt>

2147749932 (0x8004102C)
</dt> <dt>



Une tentative non conforme a été effectuée pour créer un singleton de classe, par exemple lorsque la classe est dérivée d’une classe non Singleton.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_CIM_TYPE"></span><span id="wbem_e_invalid_cim_type"></span>**WBEM \_ E \_ \_ type CIM non valide \_**
</dt> <dd> <dl> <dt>

2147749933 (0x8004102D)
</dt> <dt>



Le type CIM spécifié n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**WBEM \_ E \_ , \_ méthode non valide**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



La méthode demandée n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_paramètres de méthode WBEM E \_ non valides \_ \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Les paramètres fournis pour la méthode ne sont pas valides.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYSTEM_PROPERTY"></span><span id="wbem_e_system_property"></span>**\_ \_ propriété système WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749936 (0x80041030)
</dt> <dt>



Une tentative a été effectuée pour obtenir des qualificateurs sur une propriété système.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PROPERTY"></span><span id="wbem_e_invalid_property"></span>**\_ \_ propriété non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749937 (0x80041031)
</dt> <dt>



Le type de propriété n’est pas reconnu.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CALL_CANCELLED"></span><span id="wbem_e_call_cancelled"></span>**\_appel d’E WBEM \_ \_ annulé**
</dt> <dd> <dl> <dt>

2147749938 (0x80041032)
</dt> <dt>



Le processus asynchrone a été annulé en interne ou par l’utilisateur. Notez qu’en raison de la durée et de la nature de l’opération asynchrone, l’opération n’a peut-être pas été réellement annulée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SHUTTING_DOWN"></span><span id="wbem_e_shutting_down"></span>**fermeture de WBEM \_ E \_ \_**
</dt> <dd> <dl> <dt>

2147749939 (0x80041033)
</dt> <dt>



L’utilisateur a demandé une opération alors que WMI est en cours d’arrêt.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPAGATED_METHOD"></span><span id="wbem_e_propagated_method"></span>**\_ \_ méthode propagée d’E WBEM \_**
</dt> <dd> <dl> <dt>

2147749940 (0x80041034)
</dt> <dt>



Une tentative de réutilisation d’un nom de méthode existant à partir d’une classe parente a été effectuée et les signatures ne correspondent pas.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PARAMETER"></span><span id="wbem_e_unsupported_parameter"></span>**\_ \_ paramètre non pris en charge par WBEM E \_**
</dt> <dd> <dl> <dt>

2147749941 (0x80041035)
</dt> <dt>



Une ou plusieurs valeurs de paramètre, telles qu'un texte de requête, sont trop complexes ou non prises en charge. WMI est donc invité à réessayer l’opération avec des paramètres plus simples.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_PARAMETER_ID"></span><span id="wbem_e_missing_parameter_id"></span>**\_ID de \_ \_ paramètre manquant \_ dans WBEM E**
</dt> <dd> <dl> <dt>

2147749942 (0x80041036)
</dt> <dt>



Le paramètre était manquant dans l’appel de la méthode.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER_ID"></span><span id="wbem_e_invalid_parameter_id"></span>**\_ID de paramètre WBEM E \_ non valide \_ \_**
</dt> <dd> <dl> <dt>

2147749943 (0x80041037)
</dt> <dt>



Le paramètre de la méthode a un qualificateur d' [**ID**](standard-wmi-qualifiers.md) qui n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NONCONSECUTIVE_PARAMETER_IDS"></span><span id="wbem_e_nonconsecutive_parameter_ids"></span>**\_ID de paramètres WBEM E \_ inconsécutifs \_ \_**
</dt> <dd> <dl> <dt>

2147749944 (0x80041038)
</dt> <dt>



Un ou plusieurs des paramètres de méthode ont des qualificateurs d' [**ID**](standard-wmi-qualifiers.md) qui sont hors séquence.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PARAMETER_ID_ON_RETVAL"></span><span id="wbem_e_parameter_id_on_retval"></span>**\_ \_ ID de paramètre WBEM E \_ \_ sur \_ retVal**
</dt> <dd> <dl> <dt>

2147749945 (0x80041039)
</dt> <dt>



La valeur de retour d’une méthode a un qualificateur d' [**ID**](standard-wmi-qualifiers.md) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**WBEM \_ E \_ \_ chemin d’objet non valide \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



Le chemin d’accès à l’objet spécifié n’était pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_DISK_SPACE"></span><span id="wbem_e_out_of_disk_space"></span>**\_ \_ \_ \_ espace disque insuffisant pour \_ WBEM**
</dt> <dd> <dl> <dt>

2147749947 (0x8004103B)
</dt> <dt>



L’espace disque est insuffisant ou la limite de 4 Go sur le référentiel WMI (espace de stockage CIM) est atteinte.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BUFFER_TOO_SMALL"></span><span id="wbem_e_buffer_too_small"></span>**\_ \_ mémoire tampon WBEM E \_ trop \_ petite**
</dt> <dd> <dl> <dt>

2147749948 (0x8004103C)
</dt> <dt>



La mémoire tampon fournie est trop petite pour contenir tous les objets de l’énumérateur ou pour lire une propriété de type chaîne.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_PUT_EXTENSION"></span><span id="wbem_e_unsupported_put_extension"></span>**\_extension d' \_ put non prise en charge par WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749949 (0x8004103D)
</dt> <dt>



Le fournisseur ne prend pas en charge l’opération put demandée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_OBJECT_TYPE"></span><span id="wbem_e_unknown_object_type"></span>**\_type d' \_ \_ objet inconnu WBEM E \_**
</dt> <dd> <dl> <dt>

2147749950 (0x8004103E)
</dt> <dt>



Un objet avec un type ou une version incorrect a été rencontré pendant le marshaling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNKNOWN_PACKET_TYPE"></span><span id="wbem_e_unknown_packet_type"></span>**\_type de \_ \_ paquet inconnu \_ WBEM**
</dt> <dd> <dl> <dt>

2147749951 (0x8004103F)
</dt> <dt>



Un paquet avec un type ou une version incorrect a été rencontré pendant le marshaling.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_VERSION_MISMATCH"></span><span id="wbem_e_marshal_version_mismatch"></span>**incompatibilité de \_ \_ version de MARSHALing WBEM \_ \_**
</dt> <dd> <dl> <dt>

2147749952 (0x80041040)
</dt> <dt>



La version du paquet n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MARSHAL_INVALID_SIGNATURE"></span><span id="wbem_e_marshal_invalid_signature"></span>**\_ \_ \_ signature non valide du \_ Marshal WBEM**
</dt> <dd> <dl> <dt>

2147749953 (0x80041041)
</dt> <dt>



Le paquet semble endommagé.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUALIFIER"></span><span id="wbem_e_invalid_qualifier"></span>**\_qualificateur E \_ non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749954 (0x80041042)
</dt> <dt>



Tentative d’incompatibilité de qualificateurs, par exemple en \[ plaçant \] une clé sur un objet au lieu d’une propriété.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_DUPLICATE_PARAMETER"></span><span id="wbem_e_invalid_duplicate_parameter"></span>**\_ \_ \_ paramètre en double non valide pour WBEM \_**
</dt> <dd> <dl> <dt>

2147749955 (0x80041043)
</dt> <dt>



Un paramètre en double a été déclaré dans une méthode CIM.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MUCH_DATA"></span><span id="wbem_e_too_much_data"></span>**WBEM \_ E \_ de \_ données trop nombreuses \_**
</dt> <dd> <dl> <dt>

2147749956 (0x80041044)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SERVER_TOO_BUSY"></span><span id="wbem_e_server_too_busy"></span>**\_serveur WBEM \_ E \_ encombré \_**
</dt> <dd> <dl> <dt>

2147749957 (0x80041045)
</dt> <dt>



L’appel à [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) a échoué. Le fournisseur peut réactiver l’événement.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_FLAVOR"></span><span id="wbem_e_invalid_flavor"></span>**\_version WBEM E \_ non valide \_**
</dt> <dd> <dl> <dt>

2147749958 (0x80041046)
</dt> <dt>



La version de qualificateur spécifiée n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CIRCULAR_REFERENCE"></span><span id="wbem_e_circular_reference"></span>**\_ \_ référence circulaire WBEM \_ E**
</dt> <dd> <dl> <dt>

2147749959 (0x80041047)
</dt> <dt>



Une tentative de création d’une référence circulaire (par exemple, la dérivation d’une classe à partir d’elle-même) a été effectuée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_CLASS_UPDATE"></span><span id="wbem_e_unsupported_class_update"></span>**\_ \_ \_ mise à jour de classe non prise en charge par WBEM \_**
</dt> <dd> <dl> <dt>

2147749960 (0x80041048)
</dt> <dt>



La classe spécifiée n’est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_KEY_INHERITANCE"></span><span id="wbem_e_cannot_change_key_inheritance"></span>**WBEM \_ E \_ ne peut pas \_ modifier \_ \_ l’héritage de la clé**
</dt> <dd> <dl> <dt>

2147749961 (0x80041049)
</dt> <dt>



Tentative de modification d’une clé lorsque des instances ou des sous-classes utilisent déjà la clé.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_CHANGE_INDEX_INHERITANCE"></span><span id="wbem_e_cannot_change_index_inheritance"></span>**WBEM \_ E \_ ne peut pas \_ modifier \_ \_ l’héritage d’index**
</dt> <dd> <dl> <dt>

2147749968 (0x80041050)
</dt> <dt>



Une tentative a été effectuée pour modifier un index lorsque des instances ou des sous-classes utilisent déjà l’index.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TOO_MANY_PROPERTIES"></span><span id="wbem_e_too_many_properties"></span>**WBEM \_ E \_ trop \_ de \_ Propriétés**
</dt> <dd> <dl> <dt>

2147749969 (0x80041051)
</dt> <dt>



Une tentative de création de propriétés supplémentaires que la version actuelle de la classe prend en charge a été effectuée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_TYPE_MISMATCH"></span><span id="wbem_e_update_type_mismatch"></span>**incompatibilité de \_ \_ type de mise à jour WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749970 (0x80041052)
</dt> <dt>



La propriété a été redéfinie avec un type en conflit dans une classe dérivée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_OVERRIDE_NOT_ALLOWED"></span><span id="wbem_e_update_override_not_allowed"></span>**REMPLACEMENT de la \_ \_ mise à jour WBEM E \_ \_ non \_ autorisé**
</dt> <dd> <dl> <dt>

2147749971 (0x80041053)
</dt> <dt>



Une tentative a été effectuée dans une classe dérivée pour substituer un qualificateur qui ne peut pas être substitué.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UPDATE_PROPAGATED_METHOD"></span><span id="wbem_e_update_propagated_method"></span>**\_méthode de \_ mise à jour \_ propagée WBEM \_**
</dt> <dd> <dl> <dt>

2147749972 (0x80041054)
</dt> <dt>



La méthode a été déclarée à nouveau avec une signature en conflit dans une classe dérivée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NOT_IMPLEMENTED"></span><span id="wbem_e_method_not_implemented"></span>**\_méthode WBEM \_ E \_ non \_ implémentée**
</dt> <dd> <dl> <dt>

2147749973 (0x80041055)
</dt> <dt>



Une tentative d’exécution d’une méthode non marquée avec \[ implémentée \] dans une classe pertinente a été effectuée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_DISABLED"></span><span id="wbem_e_method_disabled"></span>**\_méthode WBEM \_ E \_ désactivée**
</dt> <dd> <dl> <dt>


</dt> <dt>



Une tentative d’exécution d’une méthode marquée avec l’option \[ Disabled a été effectuée \] .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_REFRESHER_BUSY"></span><span id="wbem_e_refresher_busy"></span>**\_actualisation E WBEM \_ \_ occupée**
</dt> <dd> <dl> <dt>

2147749975 (0x80041057)
</dt> <dt>



L’actualisateur est occupé par une autre opération.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNPARSABLE_QUERY"></span><span id="wbem_e_unparsable_query"></span>**\_requête E \_ unanalysable \_ WBEM**
</dt> <dd> <dl> <dt>

2147749976 (0x80041058)
</dt> <dt>



La syntaxe de la requête de filtrage n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_EVENT_CLASS"></span><span id="wbem_e_not_event_class"></span>**WBEM \_ E \_ not \_ , \_ classe d’événements**
</dt> <dd> <dl> <dt>

2147749977 (0x80041059)
</dt> <dt>



La clause from d’une requête de filtrage fait référence à une classe qui n’est pas une classe d’événements (non dérivée d' [**\_ \_ Event**](--event.md)).


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_GROUP_WITHIN"></span><span id="wbem_e_missing_group_within"></span>**\_ \_ \_ groupe \_ de**
</dt> <dd> <dl> <dt>

2147749978 (0x8004105A)
</dt> <dt>



Une clause GROUP BY a été utilisée sans la clause GROUP WITHIN correspondante.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_MISSING_AGGREGATION_LIST"></span><span id="wbem_e_missing_aggregation_list"></span>**\_liste d' \_ agrégation absente de WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749979 (0x8004105B)
</dt> <dt>



Une clause GROUP BY a été utilisée. L'agrégation sur toutes les propriétés n'est pas prise en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NOT_AN_OBJECT"></span><span id="wbem_e_property_not_an_object"></span>**la \_ propriété WBEM E \_ \_ n’est pas \_ un \_ objet**
</dt> <dd> <dl> <dt>

2147749980 (0x8004105C)
</dt> <dt>



La notation à points a été utilisée sur une propriété qui n'est pas un objet incorporé.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AGGREGATING_BY_OBJECT"></span><span id="wbem_e_aggregating_by_object"></span>**\_ \_ \_ l’agrégation par l' \_ objet WBEM E**
</dt> <dd> <dl> <dt>

2147749981 (0x8004105D)
</dt> <dt>



Une clause GROUP BY référence une propriété qui est un objet incorporé sans utiliser de notation à points.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNINTERPRETABLE_PROVIDER_QUERY"></span><span id="wbem_e_uninterpretable_provider_query"></span>**\_requête de \_ fournisseur ininterprétable WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749983 (0x8004105F)
</dt> <dt>



La requête d’inscription du fournisseur d’événements ([**\_ \_ EventProviderRegistration**](--eventproviderregistration.md)) n’a pas spécifié les classes pour lesquelles des événements ont été fournis.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_BACKUP_RESTORE_WINMGMT_RUNNING"></span><span id="wbem_e_backup_restore_winmgmt_running"></span>**restauration de la \_ sauvegarde WBEM E \_ \_ \_ winmgmt \_ en cours d’exécution**
</dt> <dd> <dl> <dt>

2147749984 (0x80041060)
</dt> <dt>



La demande a été faite pour sauvegarder ou restaurer le référentiel pendant qu’il était utilisé par WinMgmt.exe ou par le processus SVCHOST qui contient le service WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUEUE_OVERFLOW"></span><span id="wbem_e_queue_overflow"></span>**dépassement de la \_ \_ file d’attente WBEM E \_**
</dt> <dd> <dl> <dt>

2147749985 (0x80041061)
</dt> <dt>



Dépassement de la capacité de la file d’attente de remise asynchrone du consommateur d’événements trop lent.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PRIVILEGE_NOT_HELD"></span><span id="wbem_e_privilege_not_held"></span>**\_privilège WBEM \_ E \_ non \_ détenu**
</dt> <dd> <dl> <dt>

2147749986 (0x80041062)
</dt> <dt>



L’opération a échoué car le client n’a pas le privilège de sécurité nécessaire.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATOR"></span><span id="wbem_e_invalid_operator"></span>**WBEM \_ E \_ opérateur non valide \_**
</dt> <dd> <dl> <dt>

2147749987 (0x80041063)
</dt> <dt>



L’opérateur n’est pas valide pour ce type de propriété.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_LOCAL_CREDENTIALS"></span><span id="wbem_e_local_credentials"></span>**\_ \_ \_ informations d’identification locales WBEM**
</dt> <dd> <dl> <dt>

2147749988 (0x80041064)
</dt> <dt>



L’utilisateur a spécifié un nom d’utilisateur/mot de passe/autorité sur une connexion locale. L’utilisateur doit utiliser un nom d’utilisateur/mot de passe vide et s’appuyer sur la sécurité par défaut.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CANNOT_BE_ABSTRACT"></span><span id="wbem_e_cannot_be_abstract"></span>**WBEM \_ E \_ ne peut pas \_ être \_ abstract**
</dt> <dd> <dl> <dt>

2147749989 (0x80041065)
</dt> <dt>



La classe a été rendue abstraite lorsque sa classe parente n’est pas abstraite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMENDED_OBJECT"></span><span id="wbem_e_amended_object"></span>**WBEM \_ E a \_ modifié l' \_ objet**
</dt> <dd> <dl> <dt>

2147749990 (0x80041066)
</dt> <dt>



L’objet modifié a été écrit sans que l’indicateur **WBEM \_ \_ use \_ Modified \_ Qualifiers** ne soit spécifié.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLIENT_TOO_SLOW"></span><span id="wbem_e_client_too_slow"></span>**\_client WBEM \_ E \_ trop \_ lent**
</dt> <dd> <dl> <dt>

2147749991 (0x80041067)
</dt> <dt>



Le client n’a pas récupéré d’objets assez rapidement à partir d’une énumération. Cette constante est retournée lorsqu’un client crée un objet d’énumération, mais ne récupère pas les objets de l’énumérateur à temps, ce qui entraîne la sauvegarde des caches d’objets de l’énumérateur.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NULL_SECURITY_DESCRIPTOR"></span><span id="wbem_e_null_security_descriptor"></span>**descripteur de sécurité de WBEM \_ E \_ null \_ \_**
</dt> <dd> <dl> <dt>

2147749992 (0x80041068)
</dt> <dt>



Le descripteur de sécurité null a été utilisé.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TIMED_OUT"></span><span id="wbem_e_timed_out"></span>**délai d’attente de WBEM \_ E \_ dépassé \_**
</dt> <dd> <dl> <dt>

2147749993 (0x80041069)
</dt> <dt>



L’opération a expiré.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_ASSOCIATION"></span><span id="wbem_e_invalid_association"></span>**\_ \_ Association non valide \_ WBEM**
</dt> <dd> <dl> <dt>

2147749994
</dt> <dt>



Association non valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_AMBIGUOUS_OPERATION"></span><span id="wbem_e_ambiguous_operation"></span>**\_ \_ opération ambiguë d’E WBEM \_**
</dt> <dd> <dl> <dt>

2147749995 (0x8004106B)
</dt> <dt>



L’opération était ambiguë.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUOTA_VIOLATION"></span><span id="wbem_e_quota_violation"></span>**\_violation de \_ quota d’E WBEM \_**
</dt> <dd> <dl> <dt>

2147749996 (0x8004106C)
</dt> <dt>



WMI prend trop de mémoire. Cela peut être dû à une faible disponibilité de la mémoire ou à une consommation excessive de la mémoire par WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TRANSACTION_CONFLICT"></span><span id="wbem_e_transaction_conflict"></span>**\_conflit de \_ transactions WBEM E \_**
</dt> <dd> <dl> <dt>

2147749997 (0x8004106D)
</dt> <dt>



L’opération a entraîné un conflit de transactions.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FORCED_ROLLBACK"></span><span id="wbem_e_forced_rollback"></span>**\_ \_ restauration forcée de WBEM E \_**
</dt> <dd> <dl> <dt>

2147749998 (0x8004106E)
</dt> <dt>



La transaction a forcé une restauration.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_UNSUPPORTED_LOCALE"></span><span id="wbem_e_unsupported_locale"></span>**\_ \_ paramètres régionaux non pris en charge par WBEM \_**
</dt> <dd> <dl> <dt>

2147749999 (0x8004106F)
</dt> <dt>



Les paramètres régionaux utilisés dans l’appel ne sont pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_HANDLE_OUT_OF_DATE"></span><span id="wbem_e_handle_out_of_date"></span>**\_ \_ gestion de WBEM \_ E \_ obsolète \_**
</dt> <dd> <dl> <dt>

2147750000 (0x80041070)
</dt> <dt>



Le descripteur d’objet est obsolète.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CONNECTION_FAILED"></span><span id="wbem_e_connection_failed"></span>**échec de la \_ connexion E WBEM \_ \_**
</dt> <dd> <dl> <dt>

2147750001 (0x80041071)
</dt> <dt>



Échec de la connexion à la base de données SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_HANDLE_REQUEST"></span><span id="wbem_e_invalid_handle_request"></span>**\_demande de \_ \_ descripteur WBEM non valide \_**
</dt> <dd> <dl> <dt>

2147750002 (0x80041072)
</dt> <dt>



La requête de handle n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROPERTY_NAME_TOO_WIDE"></span><span id="wbem_e_property_name_too_wide"></span>**\_nom de propriété WBEM E \_ \_ \_ trop \_ grand**
</dt> <dd> <dl> <dt>

2147750003 (0x80041073)
</dt> <dt>



Le nom de la propriété contient plus de 255 caractères.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_CLASS_NAME_TOO_WIDE"></span><span id="wbem_e_class_name_too_wide"></span>**\_nom de \_ classe E WBEM \_ \_ trop \_ grand**
</dt> <dd> <dl> <dt>

2147750004 (0x80041074)
</dt> <dt>



Le nom de la classe contient plus de 255 caractères.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_METHOD_NAME_TOO_WIDE"></span><span id="wbem_e_method_name_too_wide"></span>**nom de la \_ méthode WBEM E \_ \_ \_ trop \_ grand**
</dt> <dd> <dl> <dt>

2147750005 (0x80041075)
</dt> <dt>



Le nom de la méthode contient plus de 255 caractères.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_QUALIFIER_NAME_TOO_WIDE"></span><span id="wbem_e_qualifier_name_too_wide"></span>**\_nom de qualificateur d’E WBEM \_ \_ \_ trop \_ grand**
</dt> <dd> <dl> <dt>

2147750006 (0x80041076)
</dt> <dt>



Le nom du qualificateur contient plus de 255 caractères.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RERUN_COMMAND"></span><span id="wbem_e_rerun_command"></span>**\_commande WBEM E \_ relancer \_**
</dt> <dd> <dl> <dt>

2147750007 (0x80041077)
</dt> <dt>



La commande SQL doit être réexécutée en raison d’un blocage dans SQL. Cela peut être retourné uniquement lorsque des données sont stockées dans une base de données SQL.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_DATABASE_VER_MISMATCH"></span><span id="wbem_e_database_ver_mismatch"></span>**\_incompatibilité \_ de la base de données WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147750008 (0x80041078)
</dt> <dt>



La version de la base de données ne correspond pas à la version que le pilote du référentiel traite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_DELETE"></span><span id="wbem_e_veto_delete"></span>**WBEM \_ E \_ veto \_ Supprimer**
</dt> <dd> <dl> <dt>

2147750009 (0x80041079)
</dt> <dt>



WMI ne peut pas exécuter l’opération de suppression, car le fournisseur ne l’autorise pas.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VETO_PUT"></span><span id="wbem_e_veto_put"></span>**WBEM \_ E \_ veto \_ put**
</dt> <dd> <dl> <dt>

2147750010 (0x8004107A)
</dt> <dt>



WMI ne peut pas exécuter l’opération Put, car le fournisseur ne l’autorise pas.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_LOCALE"></span><span id="wbem_e_invalid_locale"></span>**\_ \_ paramètres régionaux WBEM non valides \_**
</dt> <dd> <dl> <dt>

2147750016 (0x80041080)
</dt> <dt>



L’identificateur de paramètres régionaux spécifié n’est pas valide pour l’opération.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_SUSPENDED"></span><span id="wbem_e_provider_suspended"></span>**\_fournisseur WBEM \_ E \_ suspendu**
</dt> <dd> <dl> <dt>

2147750017 (0x80041081)
</dt> <dt>



Le fournisseur est suspendu.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_SYNCHRONIZATION_REQUIRED"></span><span id="wbem_e_synchronization_required"></span>**\_synchronisation WBEM \_ E \_ requise**
</dt> <dd> <dl> <dt>

2147750018 (0x80041082)
</dt> <dt>



L’objet doit être écrit dans le référentiel WMI et récupéré à nouveau avant que l’opération demandée puisse aboutir. Cette constante est retournée lorsqu’un objet doit être validé et récupéré pour voir la valeur de la propriété.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_SCHEMA"></span><span id="wbem_e_no_schema"></span>**\_schéma E \_ non \_ WBEM**
</dt> <dd> <dl> <dt>

2147750019 (0x80041083)
</dt> <dt>



L’opération ne peut pas être terminée ; aucun schéma n’est disponible.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_ALREADY_REGISTERED"></span><span id="wbem_e_provider_already_registered"></span>**le \_ fournisseur WBEM E est \_ \_ déjà \_ inscrit**
</dt> <dd> <dl> <dt>

02147750020 (0x119FD010)
</dt> <dt>



Impossible d’inscrire le fournisseur, car il est déjà inscrit.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_REGISTERED"></span><span id="wbem_e_provider_not_registered"></span>**\_fournisseur WBEM \_ E \_ non \_ inscrit**
</dt> <dd> <dl> <dt>

2147750021 (0x80041085)
</dt> <dt>



Le fournisseur n’a pas été inscrit.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_FATAL_TRANSPORT_ERROR"></span><span id="wbem_e_fatal_transport_error"></span>**\_erreur de \_ transport non récupérable \_ \_ WBEM**
</dt> <dd> <dl> <dt>

2147750022 (0x80041086)
</dt> <dt>



Une erreur de transport irrécupérable s’est produite.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ENCRYPTED_CONNECTION_REQUIRED"></span><span id="wbem_e_encrypted_connection_required"></span>**\_ \_ connexion chiffrée WBEM \_ \_ requise**
</dt> <dd> <dl> <dt>

2147750023 (0x80041087)
</dt> <dt>



L’utilisateur a tenté de définir un nom d’ordinateur ou un domaine sans connexion chiffrée.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_TIMED_OUT"></span><span id="wbem_e_provider_timed_out"></span>**délai d’attente du \_ fournisseur WBEM E \_ \_ dépassé \_**
</dt> <dd> <dl> <dt>

2147750024 (0x80041088)
</dt> <dt>



Un fournisseur n’a pas pu signaler les résultats dans le délai d’attente spécifié.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NO_KEY"></span><span id="wbem_e_no_key"></span>**\_clé E \_ non \_ WBEM**
</dt> <dd> <dl> <dt>

2147750025 (0x80041089)
</dt> <dt>



L’utilisateur a tenté de mettre une instance sans clé définie.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_DISABLED"></span><span id="wbem_e_provider_disabled"></span>**\_fournisseur WBEM \_ E \_ désactivé**
</dt> <dd> <dl> <dt>

2147750026 (0x8004108A)
</dt> <dt>



L’utilisateur a tenté d’inscrire une instance de fournisseur, mais le serveur COM pour l’instance du fournisseur a été déchargé.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_BROAD"></span><span id="wbemess_e_registration_too_broad"></span>**\_inscription WBEMESS \_ E \_ trop \_ large**
</dt> <dd> <dl> <dt>

2147753985 (0x80042001)
</dt> <dt>



L’inscription du fournisseur chevauche le domaine d’événements système.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_REGISTRATION_TOO_PRECISE"></span><span id="wbemess_e_registration_too_precise"></span>**\_inscription WBEMESS \_ E \_ trop \_ précise**
</dt> <dd> <dl> <dt>

2147753986 (0x80042002)
</dt> <dt>



Une clause WITHIN n'est pas utilisée dans cette requête.


</dt> </dl> </dd> <dt>

<span id="WBEMESS_E_AUTHZ_NOT_PRIVILEGED"></span><span id="wbemess_e_authz_not_privileged"></span>**WBEMESS \_ E \_ auth \_ non \_ privilégié**
</dt> <dd> <dl> <dt>

2147753987 (0x80042003)
</dt> <dt>



Cet ordinateur ne dispose pas des autorisations de domaine nécessaires pour prendre en charge les fonctions de sécurité associées à l’instance d’abonnement créée. Contactez l’administrateur de domaine pour que cet ordinateur soit ajouté au groupe d’accès d’autorisation Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RETRY_LATER"></span><span id="wbem_e_retry_later"></span>**WBEM \_ \_ Réessayer \_ plus tard**
</dt> <dd> <dl> <dt>

2147758081 (0x80043001)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_RESOURCE_CONTENTION"></span><span id="wbem_e_resource_contention"></span>**\_conflit de \_ ressources WBEM E \_**
</dt> <dd> <dl> <dt>

2147758082 (0x80043002)
</dt> <dt>



Réservé pour un usage futur.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_QUALIFIER_NAME"></span><span id="wbemmof_e_expected_qualifier_name"></span>**WBEMMOF \_ E \_ \_ nom du qualificateur attendu \_**
</dt> <dd> <dl> <dt>

2147762177 (0x80044001)
</dt> <dt>



Nom de qualificateur attendu.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_SEMI"></span><span id="wbemmof_e_expected_semi"></span>**WBEMMOF \_ E \_ attendu \_**
</dt> <dd> <dl> <dt>

2147762178 (0x80044002)
</dt> <dt>



Point-virgule ou' = 'attendu.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_BRACE"></span><span id="wbemmof_e_expected_open_brace"></span>**WBEMMOF \_ E \_ \_ accolade ouvrante attendue \_**
</dt> <dd> <dl> <dt>

2147762179 (0x80044003)
</dt> <dt>



Accolade ouvrante attendue.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACE"></span><span id="wbemmof_e_expected_close_brace"></span>**WBEMMOF \_ E \_ \_ accolade fermante attendue \_**
</dt> <dd> <dl> <dt>

2147762180 (0x80044004)
</dt> <dt>



Accolade fermante manquante ou élément de tableau non conforme.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_BRACKET"></span><span id="wbemmof_e_expected_close_bracket"></span>**WBEMMOF \_ E \_ \_ crochet fermant \_ attendu**
</dt> <dd> <dl> <dt>

2147762181 (0x80044005)
</dt> <dt>



Crochet fermant attendu.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLOSE_PAREN"></span><span id="wbemmof_e_expected_close_paren"></span>**WBEMMOF \_ E \_ \_ parenthèse fermante attendue \_**
</dt> <dd> <dl> <dt>

2147762182 (0x80044006)
</dt> <dt>



Parenthèse fermante attendue.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ILLEGAL_CONSTANT_VALUE"></span><span id="wbemmof_e_illegal_constant_value"></span>**WBEMMOF \_ E \_ \_ valeur constante non conforme \_**
</dt> <dd> <dl> <dt>

2147762183 (0x80044007)
</dt> <dt>



Valeur numérique hors limites ou chaînes sans guillemets.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_TYPE_IDENTIFIER"></span><span id="wbemmof_e_expected_type_identifier"></span>**WBEMMOF \_ E \_ \_ identificateur de type attendu \_**
</dt> <dd> <dl> <dt>

2147762184 (0x80044008)
</dt> <dt>



Identificateur de type attendu.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_OPEN_PAREN"></span><span id="wbemmof_e_expected_open_paren"></span>**WBEMMOF \_ E \_ \_ parenthèse ouverte attendue \_**
</dt> <dd> <dl> <dt>

2147762185 (0x80044009)
</dt> <dt>



Parenthèse ouverte attendue.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TOKEN"></span><span id="wbemmof_e_unrecognized_token"></span>**WBEMMOF \_ E \_ jeton non reconnu \_**
</dt> <dd> <dl> <dt>

2147762186 (0x8004400A)
</dt> <dt>



Jeton inattendu dans le fichier.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNRECOGNIZED_TYPE"></span><span id="wbemmof_e_unrecognized_type"></span>**WBEMMOF \_ E \_ type non reconnu \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Identificateur de type non reconnu ou non pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_PROPERTY_NAME"></span><span id="wbemmof_e_expected_property_name"></span>**WBEMMOF \_ E \_ nom de la propriété attendue \_ \_**
</dt> <dd> <dl> <dt>

2147762187 (0x8004400B)
</dt> <dt>



Nom de la propriété ou de la méthode attendu.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPEDEF_NOT_SUPPORTED"></span><span id="wbemmof_e_typedef_not_supported"></span>**WBEMMOF \_ E \_ typedef \_ non \_ pris en charge**
</dt> <dd> <dl> <dt>

2147762189 (0x8004400D)
</dt> <dt>



Les typedefs et les types énumérés ne sont pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ALIAS"></span><span id="wbemmof_e_unexpected_alias"></span>**WBEMMOF \_ E \_ \_ alias inattendu**
</dt> <dd> <dl> <dt>

2147762190 (0x8004400E)
</dt> <dt>



Seule une référence à un objet de classe peut avoir une valeur d’alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNEXPECTED_ARRAY_INIT"></span><span id="wbemmof_e_unexpected_array_init"></span>**WBEMMOF \_ E \_ inattendue de \_ tableau \_ init**
</dt> <dd> <dl> <dt>

2147762191 (0x8004400F)
</dt> <dt>



Initialisation de tableau inattendue. Les tableaux doivent être déclarés avec \[ \] .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_AMENDMENT_SYNTAX"></span><span id="wbemmof_e_invalid_amendment_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe d’amendement non valide \_**
</dt> <dd> <dl> <dt>

2147762192 (0x80044010)
</dt> <dt>



La syntaxe du chemin d’accès de l’espace de noms n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DUPLICATE_AMENDMENT"></span><span id="wbemmof_e_invalid_duplicate_amendment"></span>**WBEMMOF \_ E \_ \_ Amendement dupliqué non valide \_**
</dt> <dd> <dl> <dt>

2147762193 (0x80044011)
</dt> <dt>



Spécificateurs d’amendement en double.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_PRAGMA"></span><span id="wbemmof_e_invalid_pragma"></span>**WBEMMOF \_ E \_ pragma non valide \_**
</dt> <dd> <dl> <dt>

2147762194 (0x80044012)
</dt> <dt>



le [ \# pragma](pragma-namespace.md) doit être suivi d’un mot clé valide.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SYNTAX"></span><span id="wbemmof_e_invalid_namespace_syntax"></span>**WBEMMOF \_ E \_ syntaxe d’espace de noms non valide \_ \_**
</dt> <dd> <dl> <dt>

2147762195 (0x80044013)
</dt> <dt>



La syntaxe du chemin d’accès de l’espace de noms n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_CLASS_NAME"></span><span id="wbemmof_e_expected_class_name"></span>**WBEMMOF \_ E \_ \_ nom de classe attendu \_**
</dt> <dd> <dl> <dt>

2147762196 (0x80044014)
</dt> <dt>



Un caractère inattendu dans le nom de la classe doit être un identificateur.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_TYPE_MISMATCH"></span><span id="wbemmof_e_type_mismatch"></span>**incompatibilité de \_ type E WBEMMOF \_ \_**
</dt> <dd> <dl> <dt>

2147762197 (0x80044015)
</dt> <dt>



La valeur spécifiée ne peut pas être transformée dans le type approprié.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_ALIAS_NAME"></span><span id="wbemmof_e_expected_alias_name"></span>**WBEMMOF \_ E \_ \_ nom d’alias attendu \_**
</dt> <dd> <dl> <dt>

2147762198 (0x80044016)
</dt> <dt>



Le signe dollar doit être suivi d’un nom d’alias en tant qu’identificateur.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_CLASS_DECLARATION"></span><span id="wbemmof_e_invalid_class_declaration"></span>**WBEMMOF \_ E \_ \_ déclaration de classe non valide \_**
</dt> <dd> <dl> <dt>

2147762199 (0x80044017)
</dt> <dt>



La déclaration de classe n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_INSTANCE_DECLARATION"></span><span id="wbemmof_e_invalid_instance_declaration"></span>**WBEMMOF \_ E \_ \_ déclaration d’instance non valide \_**
</dt> <dd> <dl> <dt>

2147762200 (0x80044018)
</dt> <dt>



La déclaration d’instance n’est pas valide. Il doit commencer par « instance de »


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_DOLLAR"></span><span id="wbemmof_e_expected_dollar"></span>**WBEMMOF \_ E \_ \_ dollar ATTENDU**
</dt> <dd> <dl> <dt>

2147762201 (0x80044019)
</dt> <dt>



Signe dollar attendu. Un alias au format « $name » doit suivre le mot clé « As ».


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_CIMTYPE_QUALIFIER"></span><span id="wbemmof_e_cimtype_qualifier"></span>**\_QUALIFICATEUR WBEMMOF E \_ CimType \_**
</dt> <dd> <dl> <dt>

2147762202 (0x8004401A)
</dt> <dt>



Le qualificateur « CIMTYPE » ne peut pas être spécifié directement dans un fichier MOF. Utilisez la notation de type standard.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_PROPERTY"></span><span id="wbemmof_e_duplicate_property"></span>**WBEMMOF \_ E \_ , \_ propriété dupliquée**
</dt> <dd> <dl> <dt>

2147762203 (0x8004401B)
</dt> <dt>



Un nom de propriété dupliqué a été trouvé dans le MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_NAMESPACE_SPECIFICATION"></span><span id="wbemmof_e_invalid_namespace_specification"></span>**WBEMMOF \_ E \_ spécification d’espace de noms non valide \_ \_**
</dt> <dd> <dl> <dt>

2147762204 (0x8004401C)
</dt> <dt>



La syntaxe de l’espace de noms n’est pas valide. Les références à d’autres serveurs ne sont pas autorisées.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_OUT_OF_RANGE"></span><span id="wbemmof_e_out_of_range"></span>**WBEMMOF \_ E \_ hors \_ \_ limites**
</dt> <dd> <dl> <dt>

2147762205 (0x8004401D)
</dt> <dt>



Valeur hors limites.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FILE"></span><span id="wbemmof_e_invalid_file"></span>**WBEMMOF \_ E \_ fichier non valide \_**
</dt> <dd> <dl> <dt>

2147762206 (0x8004401E)
</dt> <dt>



Le fichier n’est pas un fichier MOF de texte valide ou un fichier MOF binaire.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ALIASES_IN_EMBEDDED"></span><span id="wbemmof_e_aliases_in_embedded"></span>**\_alias WBEMMOF E \_ \_ dans \_ Embedded**
</dt> <dd> <dl> <dt>

2147762207 (0x8004401F)
</dt> <dt>



Les objets incorporés ne peuvent pas être des alias.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NULL_ARRAY_ELEM"></span><span id="wbemmof_e_null_array_elem"></span>**WBEMMOF \_ E \_ \_ tableau null \_ elem**
</dt> <dd> <dl> <dt>

2147762208 (0x80044020)
</dt> <dt>



Les éléments NULL d’un tableau ne sont pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_DUPLICATE_QUALIFIER"></span><span id="wbemmof_e_duplicate_qualifier"></span>**\_QUALIFICATEUR WBEMMOF E \_ dupliqué \_**
</dt> <dd> <dl> <dt>

2147762209 (0x80044021)
</dt> <dt>



Le qualificateur a été utilisé plusieurs fois sur l’objet.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_FLAVOR_TYPE"></span><span id="wbemmof_e_expected_flavor_type"></span>**WBEMMOF \_ E \_ \_ type de version attendu \_**
</dt> <dd> <dl> <dt>

2147762210 (0x80044022)
</dt> <dt>



Type de version attendu, tel que **ToInstance**, **ToSubClass**, **EnableOverride** ou **DisableOverride**.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES"></span><span id="wbemmof_e_incompatible_flavor_types"></span>**WBEMMOF \_ E \_ types de version incompatibles \_ \_**
</dt> <dd> <dl> <dt>

2147762211 (0x80044023)
</dt> <dt>



La combinaison de **EnableOverride** et de **DisableOverride** sur le même qualificateur n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MULTIPLE_ALIASES"></span><span id="wbemmof_e_multiple_aliases"></span>**WBEMMOF \_ E \_ \_ alias multiples**
</dt> <dd> <dl> <dt>

2147762212 (0x80044024)
</dt> <dt>



Un alias ne peut pas être utilisé deux fois.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INCOMPATIBLE_FLAVOR_TYPES2"></span><span id="wbemmof_e_incompatible_flavor_types2"></span>**WBEMMOF \_ E \_ \_ TYPES2 version incompatible \_**
</dt> <dd> <dl> <dt>

2147762213 (0x80044025)
</dt> <dt>



La combinaison de **Restricted**, de **ToInstance** ou de **ToSubClass** n’est pas autorisée.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_NO_ARRAYS_RETURNED"></span><span id="wbemmof_e_no_arrays_returned"></span>**WBEMMOF \_ E \_ aucun \_ tableau \_ retourné**
</dt> <dd> <dl> <dt>

2147762214 (0x80044026)
</dt> <dt>



Les méthodes ne peuvent pas retourner de valeurs de tableau.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_MUST_BE_IN_OR_OUT"></span><span id="wbemmof_e_must_be_in_or_out"></span>**WBEMMOF \_ E \_ doit \_ être \_ in \_ ou \_ out**
</dt> <dd> <dl> <dt>

2147762215 (0x80044027)
</dt> <dt>



Les arguments doivent avoir un qualificateur **in** ou **out** .


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_FLAGS_SYNTAX"></span><span id="wbemmof_e_invalid_flags_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe des indicateurs non valides \_**
</dt> <dd> <dl> <dt>

2147762216 (0x80044028)
</dt> <dt>



La syntaxe des indicateurs n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_EXPECTED_BRACE_OR_BAD_TYPE"></span><span id="wbemmof_e_expected_brace_or_bad_type"></span>**WBEMMOF \_ E \_ \_ accolade attendue \_ ou \_ type incorrect \_**
</dt> <dd> <dl> <dt>

2147762217 (0x80044029)
</dt> <dt>



La dernière accolade et le point-virgule pour une classe sont manquants.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_QUAL_VALUE"></span><span id="wbemmof_e_unsupported_cimv22_qual_value"></span>**WBEMMOF \_ E \_ valeur de la \_ Qualys CIMV22 non prise en charge \_ \_**
</dt> <dd> <dl> <dt>

2147762218 (0x8004402A)
</dt> <dt>



Une fonctionnalité CIM version 2,2 n’est pas prise en charge pour une valeur de qualificateur.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_UNSUPPORTED_CIMV22_DATA_TYPE"></span><span id="wbemmof_e_unsupported_cimv22_data_type"></span>**WBEMMOF \_ E \_ \_ type de données CIMV22 \_ non pris en charge \_**
</dt> <dd> <dl> <dt>

2147762219 (0x8004402B)
</dt> <dt>



Le type de données CIM version 2,2 n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETEINSTANCE_SYNTAX"></span><span id="wbemmof_e_invalid_deleteinstance_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe DELETEINSTANCE non valide \_**
</dt> <dd> <dl> <dt>

2147762220 (0x8004402C)
</dt> <dt>



La syntaxe de suppression d’instance n’est pas valide. Elle doit être `#pragma DeleteInstance("instancepath", FAIL|NOFAIL)`


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_QUALIFIER_SYNTAX"></span><span id="wbemmof_e_invalid_qualifier_syntax"></span>**WBEMMOF \_ E \_ syntaxe de qualificateur non valide \_ \_**
</dt> <dd> <dl> <dt>

2147762221 (0x8004402D)
</dt> <dt>



La syntaxe du qualificateur n’est pas valide. Elle doit avoir la valeur `qualifiername:type=value,scope(class|instance), flavorname`.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_QUALIFIER_USED_OUTSIDE_SCOPE"></span><span id="wbemmof_e_qualifier_used_outside_scope"></span>**\_QUALIFICATEUR WBEMMOF E \_ \_ utilisé \_ en dehors de l' \_ étendue**
</dt> <dd> <dl> <dt>

2147762222 (0x8004402E)
</dt> <dt>



Le qualificateur est utilisé en dehors de son étendue.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_CREATING_TEMP_FILE"></span><span id="wbemmof_e_error_creating_temp_file"></span>**WBEMMOF \_ E \_ erreur lors de la \_ création du \_ \_ fichier temporaire**
</dt> <dd> <dl> <dt>

2147762223 (0x8004402F)
</dt> <dt>



Erreur lors de la création du fichier temporaire. Le fichier temporaire est une étape intermédiaire de la compilation MOF.


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_ERROR_INVALID_INCLUDE_FILE"></span><span id="wbemmof_e_error_invalid_include_file"></span>**\_erreur WBEMMOF \_ E \_ \_ fichier include non valide \_**
</dt> <dd> <dl> <dt>

2147762224 (0x80044030)
</dt> <dt>



Un fichier inclus dans le fichier MOF par la commande de préprocesseur n’est pas valide. [ \# ](-include.md)


</dt> </dl> </dd> <dt>

<span id="WBEMMOF_E_INVALID_DELETECLASS_SYNTAX"></span><span id="wbemmof_e_invalid_deleteclass_syntax"></span>**WBEMMOF \_ E \_ \_ syntaxe DELETECLASS non valide \_**
</dt> <dd> <dl> <dt>

2147762225 (0x80044031)
</dt> <dt>



La syntaxe des commandes de préprocesseur [ \# pragma DeleteInstance](pragma-deleteinstance.md) ou [ \# pragma deleteclass](pragma-deleteclass.md) n’est pas valide.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| En-tête<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de retour WMI](wmi-return-codes.md)
</dt> </dl>

 

