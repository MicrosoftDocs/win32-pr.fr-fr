---
title: Exigences de capteur pour la biométrie sécurisée
description: Exigences de capteur pour la biométrie sécurisée
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509858"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="0dd9c-103">Exigences de capteur pour la biométrie sécurisée</span><span class="sxs-lookup"><span data-stu-id="0dd9c-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="0dd9c-104">Microsoft s’appuie sur Module de plateforme sécurisée (TPM) (TPM) 2,0 pour s’assurer que, sur le matériel approprié, les logiciels (et y compris les logiciels malveillants au niveau du noyau) ne peuvent pas générer une authentification biométrique valide si la biométrique de l’utilisateur n’a pas été fournie au moment de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="0dd9c-105">Pour ce faire, nous utilisons des autorisations basées sur une session TPM 2,0 et le capteur effectuant l’extraction et la correspondance des fonctionnalités dans un environnement d’exécution approuvé.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="0dd9c-106">La première fois que le Windows Biometric Framework voit un capteur sécurisé (tel qu’il est signalé par la fonctionnalité de capteur sécurisé), il provisionne un secret partagé entre le capteur biométrique sécurisé et le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="0dd9c-107">Ce secret n’est jamais exposé au système d’exploitation et il est propre à chaque capteur.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="0dd9c-108">Pour effectuer une authentification, le Windows Biometric Framework ouvre une session avec le module de plateforme sécurisée et obtient une valeur à usage unique.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="0dd9c-109">La valeur à usage unique est transmise au capteur sécurisé dans le cadre d’une opération de correspondance sécurisée.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="0dd9c-110">Le capteur effectue la correspondance dans l’environnement d’exécution approuvé et, si elle réussit, calcule un HMAC sur ce nonce et l’identité de l’utilisateur identifié.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="0dd9c-111">Ce HMAC peut être utilisé par le Windows Biometric Framework pour effectuer des opérations de chiffrement dans le module de plateforme sécurisée pour l’utilisateur identifié.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="0dd9c-112">Le HMAC est de courte durée et expire après quelques secondes.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="0dd9c-113">À l’aide de ce protocole, après l’approvisionnement initial, aucune donnée sensible n’est contenue dans le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="0dd9c-114">Les secrets sont détenus par le TPM et le capteur sécurisé, et la seule chose exposée pendant l’authentification est le HMAC de courte durée.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="0dd9c-115">Capacité de capteur sécurisée</span><span class="sxs-lookup"><span data-stu-id="0dd9c-115">Secure sensor capability</span></span>

<span data-ttu-id="0dd9c-116">La \_ fonctionnalité de \_ capteur sécurisé de capacité WINBIO \_ doit être signalée par le capteur si elle prend en charge les nouvelles méthodes d’adaptateur de moteur dans v 4,0 de l’interface de l’adaptateur de moteur.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="0dd9c-117">Pour affirmer qu’un capteur est un capteur sécurisé, il doit remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0dd9c-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="0dd9c-118">Le moteur correspondant du capteur doit être isolé du système d’exploitation normal (par exemple, à l’aide d’un environnement d’exécution approuvé)</span><span class="sxs-lookup"><span data-stu-id="0dd9c-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="0dd9c-119">Le capteur doit prendre en charge l’entrée sécurisée d’exemples dans le moteur de correspondance isolé ; le contenu des exemples ne doit jamais être exposé au système d’exploitation normal</span><span class="sxs-lookup"><span data-stu-id="0dd9c-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="0dd9c-120">Le moteur de correspondance doit prendre en charge la version sécurisée des informations d’identification en implémentant les nouvelles méthodes v4 présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="0dd9c-121">Le capteur doit prendre en charge la détection d’attaques de présentation.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="0dd9c-122">La \_ valeur du \_ capteur sécurisé de capacité WINBIO \_ est contenue dans la structure de [**\_ fonctionnalités WINBIO**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) .</span><span class="sxs-lookup"><span data-stu-id="0dd9c-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="0dd9c-123">Voici un exemple de la façon de le définir.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="0dd9c-124">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0dd9c-124">Error Codes</span></span>


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="0dd9c-125">Interface de l’adaptateur de moteur v 4,0</span><span class="sxs-lookup"><span data-stu-id="0dd9c-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="0dd9c-126">La version de l’interface de l’adaptateur du moteur a été incrémentée à 4,0.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="0dd9c-127">Les fonctions supplémentaires de la nouvelle interface permettent au capteur de participer au module TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0dd9c-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="0dd9c-128">Les voici :</span><span class="sxs-lookup"><span data-stu-id="0dd9c-128">They are:</span></span>

-   [<span data-ttu-id="0dd9c-129">**EngineAdapterCreateKey**</span><span class="sxs-lookup"><span data-stu-id="0dd9c-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="0dd9c-130">**EngineAdapterIdentifyFeatureSetSecure**</span><span class="sxs-lookup"><span data-stu-id="0dd9c-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a><span data-ttu-id="0dd9c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dd9c-131">Requirements</span></span>

<span data-ttu-id="0dd9c-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="0dd9c-132">Windows 10</span></span>

 

 