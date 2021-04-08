---
title: Propriétés de la méthode EAP (Eaptypes. h)
description: Utilisé par les demandeurs et les authentificateurs pour déterminer les méthodes EAP à utiliser avec un demandeur ou un authentificateur donné. Les propriétés de méthode spécifient également la configuration d’une méthode.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741845"
---
# <a name="eap-method-properties"></a><span data-ttu-id="d5f4c-104">Propriétés de la méthode EAP</span><span class="sxs-lookup"><span data-stu-id="d5f4c-104">EAP Method Properties</span></span>

<span data-ttu-id="d5f4c-105">Utilisé par les demandeurs et les authentificateurs pour déterminer les méthodes EAP à utiliser avec un demandeur ou un authentificateur donné.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="d5f4c-106">Les propriétés de méthode spécifient également la configuration d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="d5f4c-107">Par exemple, le demandeur [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) peut exiger que des méthodes aient certaines propriétés à utiliser avec le demandeur [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="d5f4c-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="d5f4c-108">Le matériel de génération de clé, par exemple, est une exigence.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="d5f4c-109">Les propriétés prises en charge par les méthodes EAP sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="d5f4c-110">Les propriétés sont stockées sous la forme de valeurs de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="d5f4c-111">Pour plus d’informations, consultez la section clé de registre DLL de méthode d’homologue EAP de la rubrique [configuration du Registre pour les méthodes EAP.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="d5f4c-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="d5f4c-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d5f4c-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-114">La méthode permet à la suite de chiffrement d’être négociée dans le cadre du chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="d5f4c-115">Windows Server 2008 prend en charge les [suites de chiffrement](/windows/desktop/SecAuthN/tls-cipher-suites)3DES suivantes :</span><span class="sxs-lookup"><span data-stu-id="d5f4c-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="d5f4c-116">TLS \_ RSA \_ avec \_ 3DES \_ Ede \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="d5f4c-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="d5f4c-117">TLS \_ dhe \_ DSS \_ avec \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="d5f4c-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="d5f4c-118">SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5 (SSL 2 s’il est activé)</span><span class="sxs-lookup"><span data-stu-id="d5f4c-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="d5f4c-119">Pour plus d’informations sur le protocole de sécurité TLS 1,0, consultez [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="d5f4c-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d5f4c-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-122">La méthode fournit un échange dans lequel l’authentificateur authentifie l’homologue et vice versa.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d5f4c-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-125">La méthode fournit l’authentification de l’origine des données et la protection contre toute modification non autorisée des informations pour les paquets EAP, y compris les demandes et les réponses EAP.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="d5f4c-126">Quand vous effectuez cette revendication, une spécification de méthode doit spécifier les paquets EAP protégés et les champs protégés dans les paquets EAP.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d5f4c-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-129">La méthode peut vous protéger contre la relecture d’une méthode EAP ou de ses messages.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="d5f4c-130">Impossible de relire les indications des résultats de réussite et d’échec.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d5f4c-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-133">La méthode peut chiffrer les messages EAP.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="d5f4c-134">Les demandes EAP, les réponses EAP, les indications de résultat de réussite et les indications de résultat d’échec sont chiffrées.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="d5f4c-135">Une méthode qui fait cette revendication doit prendre en charge identity protection.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="d5f4c-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-138">La méthode peut dériver un support de clé exportable, tel que la clé de session principale (MSK) et la clé de session principale étendue (EMSK).</span><span class="sxs-lookup"><span data-stu-id="d5f4c-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="d5f4c-139">Le MSK est utilisé uniquement pour une dérivation de clé supplémentaire, pas directement pour la protection de la conversation EAP ou des données ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="d5f4c-140">L’utilisation de EMSK est réservée.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="d5f4c-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-143">La longueur de clé minimale prise en charge par la méthode EAP est de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="d5f4c-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-146">La longueur de clé minimale prise en charge par la méthode EAP est de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="d5f4c-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-149">La longueur de clé minimale prise en charge par la méthode EAP est de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="d5f4c-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-152">La longueur de clé minimale prise en charge par la méthode EAP est de 512 bits.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="d5f4c-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-155">La longueur de clé minimale prise en charge par la méthode EAP est de 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="d5f4c-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-158">La méthode n’autorise pas une attaque hors connexion qui a un facteur de travail en fonction du nombre de mots de passe dans le dictionnaire d’un attaquant.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="d5f4c-159">Lorsque l’authentification par mot de passe est utilisée, les mots de passe sont couramment sélectionnés à partir d’un petit ensemble (par rapport à un ensemble de clés de N bits), ce qui soulève un problème concernant les attaques de dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="d5f4c-160">Une méthode peut être appelée à fournir une protection contre les attaques de dictionnaire si, quand elle utilise un mot de passe comme secret, la méthode n’autorise pas une attaque hors connexion qui a un facteur de travail en fonction du nombre de mots de passe dans le dictionnaire d’un attaquant.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-163">La méthode a la capacité, dans le cas où une association de sécurité a été établie précédemment, de créer une association de sécurité nouvelle ou actualisée plus efficacement ou à un plus petit nombre d’allers-retours.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-166">La méthode montre au serveur EAP qu’une entité unique a agi en tant qu’homologue EAP pour toutes les méthodes exécutées dans une méthode de tunnel.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="d5f4c-167">La liaison peut également impliquer que le serveur EAP démontre à l’homologue qu’une entité unique a agi en tant que serveur EAP pour toutes les méthodes exécutées dans le cadre d’une méthode de tunnel.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="d5f4c-168">Si elle est exécutée correctement, la liaison sert à atténuer les vulnérabilités de l’intercepteur.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-171">La méthode démontre que les attaques passives (telles que la capture de la conversation EAP) ou les attaques actives (y compris la compromission de l’MSK ou du EMSK) ne compromettent pas la MSKs ou la EMSKs ultérieure ou antérieure.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-174">La méthode peut prendre en charge la fragmentation et le réassemblage si les paquets EAP dépassent la MTU minimale (unité de transmission maximale) de 1020 octets.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-177">La méthode peut communiquer des propriétés de canal protégées par l’intégrité, telles que des identificateurs de point de terminaison, qui peuvent être comparées à des valeurs communiquées à l’aide de mécanismes hors bande, tels qu’une [authentification, une autorisation et une gestion des comptes](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) ou le protocole de couche inférieure.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d5f4c-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-180">La méthode prend en charge la protection d’accès réseau (NAP).</span><span class="sxs-lookup"><span data-stu-id="d5f4c-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-183">La méthode peut être utilisée sur un ordinateur autonome.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="d5f4c-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-186">La méthode prend en charge le chiffrement du [protocole MPPE (Microsoft Point-to-Point Encryption)](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="d5f4c-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-189">La méthode prend en charge le tunneling d’autres méthodes EAP.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-192">La méthode prend en charge les propriétés configurables et a une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-195">La méthode a été certifiée par le programme de certification EAP.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="d5f4c-196">Ce bit doit être envoyé uniquement par les méthodes EAP qui ont passé la certification.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-199">Windows 7 ou version ultérieure : la méthode peut être utilisée pour authentifier un ordinateur sur un réseau à l’aide des informations d’identification de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-202">Windows 7 ou version ultérieure : la méthode peut être utilisée pour authentifier un utilisateur sur un réseau à l’aide des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-205">Windows 7 ou version ultérieure : la méthode prend en charge l’envoi de l’identité de l’utilisateur dans un canal protégé.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-208">Windows 7 ou version ultérieure : la méthode est une méthode tunnelled et prend en charge le chaînage de méthodes EAP dans le tunnel.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-211">Windows 7 ou version ultérieure : la méthode prend en charge l’équivalence d’état partagé telle que définie dans la [norme RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span><span class="sxs-lookup"><span data-stu-id="d5f4c-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d5f4c-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span><span class="sxs-lookup"><span data-stu-id="d5f4c-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5f4c-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="d5f4c-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="d5f4c-214">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-214">Reserved.</span></span> <span data-ttu-id="d5f4c-215">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d5f4c-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5f4c-216">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5f4c-216">Requirements</span></span>



| <span data-ttu-id="d5f4c-217">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5f4c-217">Requirement</span></span> | <span data-ttu-id="d5f4c-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5f4c-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f4c-219">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f4c-219">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f4c-220">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f4c-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5f4c-221">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5f4c-221">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f4c-222">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5f4c-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5f4c-223">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5f4c-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5f4c-224"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5f4c-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f4c-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5f4c-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f4c-226">Clés de Registre pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="d5f4c-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="d5f4c-227">Constantes EAPHost communes</span><span class="sxs-lookup"><span data-stu-id="d5f4c-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

