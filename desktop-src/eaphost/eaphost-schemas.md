---
title: EAPHost et schéma hérité
description: Décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML.
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dbe40f447618a9ca0da89875521349101c1191f
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104381275"
---
# <a name="eaphost-and-legacy-schema"></a><span data-ttu-id="cdb36-103">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="cdb36-103">EAPHost and Legacy Schema</span></span>

<span data-ttu-id="cdb36-104">Cette rubrique décrit le schéma EAPHost et le schéma hérité pour créer des données XML de configuration et des informations d’identification XML.</span><span class="sxs-lookup"><span data-stu-id="cdb36-104">This topic describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span>

## <a name="about-eaphost-and-legacy-schema"></a><span data-ttu-id="cdb36-105">À propos de EAPHost et du schéma hérité</span><span class="sxs-lookup"><span data-stu-id="cdb36-105">About EAPHost and Legacy Schema</span></span>

<span data-ttu-id="cdb36-106">La création du fichier XML de configuration commence avec le schéma [eaphostconfig](eaphostconfigschema-schema.md) ; la création d’informations d’identification XML commence par le schéma [eaphostusercredentials](eaphostusercredentialsschema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="cdb36-106">Creating configuration XML commences with the [eaphostconfig](eaphostconfigschema-schema.md) schema; creating credential XML commences with the [eaphostusercredentials](eaphostusercredentialsschema-schema.md) schema.</span></span>

<span data-ttu-id="cdb36-107">Plusieurs schémas natif et hérité contiennent des éléments de schéma communs.</span><span class="sxs-lookup"><span data-stu-id="cdb36-107">Several of the native and legacy schema contain common schema elements.</span></span> <span data-ttu-id="cdb36-108">Les éléments communs utilisés dans la configuration de méthode et les informations d’identification de méthode sont abstraits dans un fichier de schéma unique, appelé « schéma commun ».</span><span class="sxs-lookup"><span data-stu-id="cdb36-108">Common elements used in method configuration and method credentials are abstracted into a single schema file, referred to as the "common schema".</span></span>

<span data-ttu-id="cdb36-109">Les termes « configuration de la méthode » et « propriétés de connexion » sont utilisés indifféremment.</span><span class="sxs-lookup"><span data-stu-id="cdb36-109">The terms "method configuration" and "connection properties" are used interchangeably.</span></span> <span data-ttu-id="cdb36-110">De même, les termes « informations d’identification de la méthode » et « propriétés de l’utilisateur » sont également utilisés indifféremment.</span><span class="sxs-lookup"><span data-stu-id="cdb36-110">Likewise, the terms "method credentials" and "user properties" are also used interchangeably.</span></span>

## <a name="eaphost-schema"></a><span data-ttu-id="cdb36-111">Schéma EAPHost</span><span class="sxs-lookup"><span data-stu-id="cdb36-111">EAPHost Schema</span></span>



| <span data-ttu-id="cdb36-112">schéma</span><span class="sxs-lookup"><span data-stu-id="cdb36-112">Schema</span></span>                                                                        | <span data-ttu-id="cdb36-113">Description</span><span class="sxs-lookup"><span data-stu-id="cdb36-113">Description</span></span>                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="cdb36-114">baseeapmethodconfig</span><span class="sxs-lookup"><span data-stu-id="cdb36-114">baseeapmethodconfig</span></span>](baseeapmethodconfigschema-schema.md)                   | <span data-ttu-id="cdb36-115">Contient des éléments de schéma de configuration communs.</span><span class="sxs-lookup"><span data-stu-id="cdb36-115">Contains common configuration schema elements.</span></span>     |
| [<span data-ttu-id="cdb36-116">baseeapmethodusercredentials</span><span class="sxs-lookup"><span data-stu-id="cdb36-116">baseeapmethodusercredentials</span></span>](baseeapmethodusercredentialsschema-schema.md) | <span data-ttu-id="cdb36-117">Contient des éléments de schéma d’informations d’identification courants.</span><span class="sxs-lookup"><span data-stu-id="cdb36-117">Contains common credential schema elements.</span></span>        |
| [<span data-ttu-id="cdb36-118">eapcommon</span><span class="sxs-lookup"><span data-stu-id="cdb36-118">eapcommon</span></span>](eapcommonschema-schema.md)                                       | <span data-ttu-id="cdb36-119">Contient la définition de l’élément **EapMethodType** .</span><span class="sxs-lookup"><span data-stu-id="cdb36-119">Contains the **EapMethodType** element definition.</span></span> |
| [<span data-ttu-id="cdb36-120">eaphostconfig</span><span class="sxs-lookup"><span data-stu-id="cdb36-120">eaphostconfig</span></span>](eaphostconfigschema-schema.md)                               | <span data-ttu-id="cdb36-121">Contient le schéma de configuration EAPHost.</span><span class="sxs-lookup"><span data-stu-id="cdb36-121">Contains EAPHost configuration schema.</span></span>             |
| [<span data-ttu-id="cdb36-122">eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="cdb36-122">eaphostusercredentials</span></span>](eaphostusercredentialsschema-schema.md)             | <span data-ttu-id="cdb36-123">Contient le schéma des informations d’identification EAPHost.</span><span class="sxs-lookup"><span data-stu-id="cdb36-123">Contains EAPHost credential schema.</span></span>                |



 

## <a name="legacy-schema"></a><span data-ttu-id="cdb36-124">Schéma hérité</span><span class="sxs-lookup"><span data-stu-id="cdb36-124">Legacy Schema</span></span>



| <span data-ttu-id="cdb36-125">schéma</span><span class="sxs-lookup"><span data-stu-id="cdb36-125">Schema</span></span>                                                                            | <span data-ttu-id="cdb36-126">Description</span><span class="sxs-lookup"><span data-stu-id="cdb36-126">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cdb36-127">baseeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-127">baseeapconnectionpropertiesv1</span></span>](baseeapconnectionpropertiesv1schema-schema.md)   | <span data-ttu-id="cdb36-128">Contient des éléments de schéma de configuration communs.</span><span class="sxs-lookup"><span data-stu-id="cdb36-128">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="cdb36-129">baseeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-129">baseeapuserpropertiesv1</span></span>](baseeapuserpropertiesv1schema-schema.md)               | <span data-ttu-id="cdb36-130">Contient des éléments de schéma d’informations d’identification courants.</span><span class="sxs-lookup"><span data-stu-id="cdb36-130">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="cdb36-131">eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-131">eapconnectionpropertiesv1</span></span>](eapconnectionpropertiesv1schema-schema.md)           | <span data-ttu-id="cdb36-132">Contient des éléments de schéma de configuration communs.</span><span class="sxs-lookup"><span data-stu-id="cdb36-132">Contains common configuration schema elements.</span></span>                                               |
| [<span data-ttu-id="cdb36-133">eapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-133">eapuserpropertiesv1</span></span>](eapuserpropertiesv1schema-schema.md)                       | <span data-ttu-id="cdb36-134">Contient des éléments de schéma d’informations d’identification courants.</span><span class="sxs-lookup"><span data-stu-id="cdb36-134">Contains common credential schema elements.</span></span>                                                  |
| [<span data-ttu-id="cdb36-135">eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-135">eaptlsconnectionpropertiesv1</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="cdb36-136">Est utilisé avec EAP-TLS pour décrire les données de configuration de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-136">Is used with EAP-TLS to describe authentication configuration data.</span></span>                          |
| [<span data-ttu-id="cdb36-137">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="cdb36-137">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="cdb36-138">Est utilisé avec EAP-TLS pour décrire les données de configuration d’authentification à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdb36-138">Is used with EAP-TLS to describe authentication configuration data beginning with Windows 7.</span></span> |
| [<span data-ttu-id="cdb36-139">eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-139">eaptlsuserpropertiesv1</span></span>](eaptlsuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="cdb36-140">Est utilisé avec EAP-TLS pour décrire les informations d’identification d’authentification et les options d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-140">Is used with EAP-TLS to describe authentication credentials and credential options.</span></span>          |
| [<span data-ttu-id="cdb36-141">mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-141">mschapv2connectionpropertiesv1</span></span>](mschapv2connectionpropertiesv1schema-schema.md) | <span data-ttu-id="cdb36-142">Est utilisé avec MS-CHAPv2 pour décrire les données de configuration de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-142">Is used with MS-CHAPv2 to describe authentication configuration data.</span></span>                        |
| [<span data-ttu-id="cdb36-143">mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-143">mschapv2userpropertiesv1</span></span>](mschapv2userpropertiesv1schema-schema.md)             | <span data-ttu-id="cdb36-144">Est utilisé avec MS-CHAPv2 pour décrire les informations d’identification d’authentification et les options d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-144">Is used with MS-CHAPv2 to describe authentication credentials and credential options.</span></span>        |
| [<span data-ttu-id="cdb36-145">mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-145">mspeapconnectionpropertiesv1</span></span>](mspeapconnectionpropertiesv1schema-schema.md)     | <span data-ttu-id="cdb36-146">Est utilisé avec PEAPv0 pour décrire les données de configuration de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-146">Is used with PEAPv0 to describe authentication configuration data.</span></span>                           |
| [<span data-ttu-id="cdb36-147">mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="cdb36-147">mspeapconnectionpropertiesv2</span></span>](mspeapconnectionpropertiesv2schema-schema.md)     | <span data-ttu-id="cdb36-148">Est utilisé avec PEAPv0 pour décrire les données de configuration d’authentification à partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdb36-148">Is used with PEAPv0 to describe authentication configuration data beginning with Windows 7.</span></span>  |
| [<span data-ttu-id="cdb36-149">mspeapuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cdb36-149">mspeapuserpropertiesv1</span></span>](mspeapuserpropertiesv1schema-schema.md)                 | <span data-ttu-id="cdb36-150">Est utilisé avec PEAPv0 pour décrire les informations d’identification d’authentification et les options d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="cdb36-150">Is used with PEAPv0 to describe authentication credentials and credential options.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="cdb36-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdb36-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb36-152">Examen des exemples de schéma EAPHost et hérité</span><span class="sxs-lookup"><span data-stu-id="cdb36-152">Reviewing EAPHost and Legacy Schema Samples</span></span>](eaphost-schemas.md)
</dt> </dl>

 

 




