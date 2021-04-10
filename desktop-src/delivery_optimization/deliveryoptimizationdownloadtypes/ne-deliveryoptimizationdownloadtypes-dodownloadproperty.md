---
title: Énumération DODownloadProperty
description: Spécifie l’ID des propriétés de l’opération de téléchargement.
keywords:
- Énumération DODownloadProperty, DODownloadProperty
topic_type:
- apiref
api_name:
- DODownloadProperty
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: bb8ec6ad8cc55239522f953c6a81a8bf7b2b62ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105334"
---
# <a name="dodownloadproperty-enumeration"></a>Énumération DODownloadProperty

L’énumération **DODownloadProperty** spécifie l’ID des propriétés de l’opération do Download. Cette énumération est utilisée par l’interface **IDODownload** et est exécutée par une valeur de type Variant, où le type de la valeur est contenu.

## <a name="syntax"></a>Syntaxe

```cpp
typedef enum _DODownloadProperty
{
  DODownloadProperty_Id = 0,
  DODownloadProperty_Uri,
  DODownloadProperty_ContentId,
  DODownloadProperty_DisplayName,
  DODownloadProperty_LocalPath,
  DODownloadProperty_HttpCustomHeaders,
  DODownloadProperty_CostPolicy,
  DODownloadProperty_SecurityFlags,
  DODownloadProperty_CallbackFreqPercent,
  DODownloadProperty_CallbackFreqSeconds,
  DODownloadProperty_NoProgressTimeoutSeconds,
  DODownloadProperty_ForegroundPriority,
  DODownloadProperty_BlockingMode,
  DODownloadProperty_CallbackInterface,
  DODownloadProperty_StreamInterface,
  DODownloadProperty_SecurityContext,
  DODownloadProperty_NetworkToken
  DODownloadProperty_CorrelationVector,
  DODownloadProperty_DecryptionInfo,
  DODownloadProperty_IntegrityCheckInfo,
  DODownloadProperty_IntegrityCheckMandatory,
  DODownloadProperty_TotalSizeBytes
} DODownloadProperty;
```

## <a name="constants"></a>Constantes

| Condition requise | Valeur |
|-|-|
| DODownloadProperty_Id | Lecture seule. Utilisez cette propriété pour récupérer l’ID qui identifie de façon unique le téléchargement. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_Uri | Utilisez cette propriété pour définir ou récupérer le chemin d’accès de l’URI distant de la ressource à télécharger. Cette propriété n’est requise que si *DODownloadProperty_ContentId* n’est pas fourni. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_ContentId | Utilisez cette propriété pour définir ou récupérer l’ID de contenu unique du téléchargement. Cette propriété n’est requise que si *DODownloadProperty_Uri* n’est pas fourni. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_DisplayName | Optionnel. Utilisez cette propriété pour définir ou obtenir le nom complet du téléchargement. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_LocalPath | Utilisez cette propriété pour définir ou récupérer le nom du chemin d’accès local pour enregistrer le fichier de téléchargement. Si le chemin d’accès n’existe pas, essayez de le créer sous les privilèges de l’appelant. Cette propriété n’est requise que si *DODownloadProperty_StreamInterface* n’a pas été fourni. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_HttpCustomHeaders | Optionnel. Utilisez cette propriété pour définir ou obtenir des en-têtes de requête HTTP personnalisés. Inclura ces en-têtes pendant les opérations de demande de fichier HTTP. Les en-têtes doivent déjà être mis en forme en tant qu’en-têtes HTTP standard. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_CostPolicy | Optionnel. Utilisez cette propriété pour définir ou recevoir l’une des valeurs d’énumération **DODownloadCostPolicy** . Le type VARIANT est VT_UI4. |
| DODownloadProperty_SecurityFlags | Facultatif en écriture seule. Utilisez cette propriété pour définir ou récupérer les indicateurs de sécurité WinHTTP standard (**WINHTTP_OPTION_SECURITY_FLAGS**). Le type VARIANT est VT_UI4.</br></br>Les indicateurs suivants sont pris en charge :</br>SECURITY_FLAG_IGNORE_CERT_CN_INVALID. Autorise un nom commun non valide dans un certificat.</br>SECURITY_FLAG_IGNORE_CERT_DATE_INVALID. Autorise une date de certificat non valide.</br>SECURITY_FLAG_IGNORE_UNKNOWN_CA. Autorise une autorité de certification non valide.</br>SECURITY_FLAG_IGNORE_CERT_WRONG_USAGE. Autorise l’établissement de l’identité d’un serveur à l’aide d’un certificat non-serveur.</br>WINHTTP_ENABLE_SSL_REVOCATION. Autorise la révocation SSL. Si cet indicateur est défini, les indicateurs ci-dessus seront ignorés. |
| DODownloadProperty_CallbackFreqPercent | Optionnel. Utilisez cette propriété pour définir ou recevoir la fréquence de rappel en fonction du pourcentage de téléchargement. Le type VARIANT est VT_UI4. |
| DODownloadProperty_CallbackFreqSeconds | Optionnel. Utilisez cette propriété pour définir ou recevoir la fréquence de rappel en fonction du temps de téléchargement. La valeur par défaut est toutes les secondes. Le type VARIANT est VT_UI4. |
| DODownloadProperty_NoProgressTimeoutSeconds | Optionnel. Utilisez cette propriété pour définir ou obtenir la longueur du délai d’attente de téléchargement pour aucune progression. La valeur minimale acceptée est 60 secondes d’aucune activité de téléchargement. Le type VARIANT est VT_UI4. |
| DODownloadProperty_ForegroundPriority | Optionnel. Utilisez cette propriété pour définir ou récupérer la priorité de téléchargement actuelle. VARIANT_TRUE valeur placera le téléchargement au premier plan avec une priorité plus élevée. La valeur par défaut est la priorité d’arrière-plan. Le type VARIANT est VT_BOOL. |
| DODownloadProperty_BlockingMode | Optionnel. Utilisez cette propriété pour définir ou récupérer le mode de blocage de téléchargement en cours. VARIANT_TRUE valeur entraîne le blocage de **IDODownload :: Start** jusqu’à ce que le téléchargement soit terminé ou que l’erreur s’est produite. La valeur par défaut est le mode non bloquant. Le type VARIANT est VT_BOOL. |
| DODownloadProperty_CallbackInterface | Optionnel. Utilisez cette propriété pour définir ou obtenir le pointeur vers l’interface **IDODownloadStatusCallback** utilisée pour les rappels de téléchargement. Le type VARIANT est VT_UNKNOWN. |
| DODownloadProperty_StreamInterface | Optionnel. Utilisez cette propriété pour définir ou obtenir le pointeur vers l’interface IStream utilisée pour le type de téléchargement de flux. Le type VARIANT est VT_UNKNOWN. |
| DODownloadProperty_SecurityContext | Facultatif en écriture seule. Utilisez cette propriété pour définir le contexte de certificat à utiliser pendant les opérations de requête HTTP. La valeur doit être composée d’octets sérialisés de CERT_CONTEXT. Le type VARIANT est (VT_ARRAY \| VT_UI1). |
| DODownloadProperty_NetworkToken | Facultatif en écriture seule. Utilisez cette propriété pour définir le jeton réseau à utiliser pendant les opérations HTTP. VARIANT_TRUE valeur entraînera la capture du jeton d’identité de l’appelant et VARIANT_FALSE supprimera le jeton existant. La valeur par défaut est le jeton de l’utilisateur connecté. Le type VARIANT est VT_BOOL. |
| DODownloadProperty_CorrelationVector | Optionnel. Définit un vecteur de corrélation spécifique à des fins de télémétrie. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_DecryptionInfo | Facultatif en écriture seule. Définit les informations de déchiffrement sous la forme d’une chaîne JSON. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_IntegrityCheckInfo | Facultatif en écriture seule. Définit l’emplacement du fichier de hachage de l’élément (PHF), utilisé par pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé. Le type VARIANT est VT_BSTR. |
| DODownloadProperty_IntegrityCheckMandatory | Optionnel. Définit un indicateur booléen indiquant si l’utilisation du fichier de hachage de la pièce (PHF) est obligatoire. Si VARIANT_TRUE, le téléchargement est abandonné en cas d’échec de la vérification de l’intégrité. Le type VARIANT est VT_BOOL. |
| DODownloadProperty_TotalSizeBytes | Optionnel. Spécifie la taille totale du téléchargement en octets. Le type VARIANT est VT_UI8. |

## <a name="requirements"></a>Configuration requise

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Client minimal pris en charge** | Windows 10, version 1809 \[ applications Win32 uniquement\] |
| **Serveur minimal pris en charge** | Windows Server, version 1809 \[ applications Win32 uniquement\] |
| **En-tête** | DeliveryOptimizationDownloadTypes. h |
