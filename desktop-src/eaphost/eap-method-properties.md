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
ms.openlocfilehash: c88c31d77b666e377cbd1911cde8b5df63d8f5c2fc750cd03a701b03af5b60ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094399"
---
# <a name="eap-method-properties"></a>Propriétés de la méthode EAP

Utilisé par les demandeurs et les authentificateurs pour déterminer les méthodes EAP à utiliser avec un demandeur ou un authentificateur donné. Les propriétés de méthode spécifient également la configuration d’une méthode.

Par exemple, le demandeur [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) peut exiger que des méthodes aient certaines propriétés à utiliser avec le demandeur [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) . Le matériel de génération de clé, par exemple, est une exigence.

Les propriétés prises en charge par les méthodes EAP sont répertoriées. Les propriétés sont stockées sous la forme de valeurs de clé de registre. Pour plus d’informations, consultez la section clé de registre DLL de méthode d’homologue EAP de la rubrique [configuration du Registre pour les méthodes EAP.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



La méthode permet à la suite de chiffrement d’être négociée dans le cadre du chiffrement des données. Windows Le serveur 2008 prend en charge les [suites de chiffrement](/windows/desktop/SecAuthN/tls-cipher-suites)3DES suivantes :

-   TLS \_ RSA \_ avec \_ 3DES \_ Ede \_ CBC \_ Sha (TLS & SSL 3)
-   TLS \_ dhe \_ DSS \_ avec \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)
-   SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ avec \_ MD5 (SSL 2 s’il est activé)

Pour plus d’informations sur le protocole de sécurité TLS 1,0, consultez [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



La méthode fournit un échange dans lequel l’authentificateur authentifie l’homologue et vice versa.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



La méthode fournit l’authentification de l’origine des données et la protection contre toute modification non autorisée des informations pour les paquets EAP, y compris les demandes et les réponses EAP. Quand vous effectuez cette revendication, une spécification de méthode doit spécifier les paquets EAP protégés et les champs protégés dans les paquets EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



La méthode peut vous protéger contre la relecture d’une méthode EAP ou de ses messages. Impossible de relire les indications des résultats de réussite et d’échec.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



La méthode peut chiffrer les messages EAP. Les demandes EAP, les réponses EAP, les indications de résultat de réussite et les indications de résultat d’échec sont chiffrées. Une méthode qui fait cette revendication doit prendre en charge identity protection.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



La méthode peut dériver un support de clé exportable, tel que la clé de session principale (MSK) et la clé de session principale étendue (EMSK). Le MSK est utilisé uniquement pour une dérivation de clé supplémentaire, pas directement pour la protection de la conversation EAP ou des données ultérieures. L’utilisation de EMSK est réservée.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



La longueur de clé minimale prise en charge par la méthode EAP est de 64 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



La longueur de clé minimale prise en charge par la méthode EAP est de 128 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



La longueur de clé minimale prise en charge par la méthode EAP est de 256 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



La longueur de clé minimale prise en charge par la méthode EAP est de 512 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La longueur de clé minimale prise en charge par la méthode EAP est de 1024 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



La méthode n’autorise pas une attaque hors connexion qui a un facteur de travail en fonction du nombre de mots de passe dans le dictionnaire d’un attaquant. Lorsque l’authentification par mot de passe est utilisée, les mots de passe sont couramment sélectionnés à partir d’un petit ensemble (par rapport à un ensemble de clés de N bits), ce qui soulève un problème concernant les attaques de dictionnaire. Une méthode peut être appelée à fournir une protection contre les attaques de dictionnaire si, quand elle utilise un mot de passe comme secret, la méthode n’autorise pas une attaque hors connexion qui a un facteur de travail en fonction du nombre de mots de passe dans le dictionnaire d’un attaquant.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



La méthode a la capacité, dans le cas où une association de sécurité a été établie précédemment, de créer une association de sécurité nouvelle ou actualisée plus efficacement ou à un plus petit nombre d’allers-retours.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



La méthode montre au serveur EAP qu’une entité unique a agi en tant qu’homologue EAP pour toutes les méthodes exécutées dans une méthode de tunnel. La liaison peut également impliquer que le serveur EAP démontre à l’homologue qu’une entité unique a agi en tant que serveur EAP pour toutes les méthodes exécutées dans le cadre d’une méthode de tunnel. Si elle est exécutée correctement, la liaison sert à atténuer les vulnérabilités de l’intercepteur.


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



La méthode démontre que les attaques passives (telles que la capture de la conversation EAP) ou les attaques actives (y compris la compromission de l’MSK ou du EMSK) ne compromettent pas la MSKs ou la EMSKs ultérieure ou antérieure.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



La méthode peut prendre en charge la fragmentation et le réassemblage si les paquets EAP dépassent la MTU minimale (unité de transmission maximale) de 1020 octets.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



La méthode peut communiquer des propriétés de canal protégées par l’intégrité, telles que des identificateurs de point de terminaison, qui peuvent être comparées à des valeurs communiquées à l’aide de mécanismes hors bande, tels qu’une [authentification, une autorisation et une gestion des comptes](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) ou le protocole de couche inférieure.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



La méthode prend en charge la protection d’accès réseau (NAP).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



La méthode peut être utilisée sur un ordinateur autonome.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



La méthode prend en charge le chiffrement du [protocole MPPE (Microsoft Point-to-Point Encryption)](https://go.microsoft.com/fwlink/p/?linkid=83915) .


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



La méthode prend en charge le tunneling d’autres méthodes EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



La méthode prend en charge les propriétés configurables et a une interface utilisateur.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



La méthode a été certifiée par le programme de certification EAP. Ce bit doit être envoyé uniquement par les méthodes EAP qui ont passé la certification.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 ou version ultérieure : la méthode peut être utilisée pour authentifier une machine sur un réseau à l’aide des informations d’identification de l’ordinateur.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 ou version ultérieure : la méthode peut être utilisée pour authentifier un utilisateur sur un réseau à l’aide des informations d’identification de l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 ou version ultérieure : la méthode prend en charge l’envoi de l’identité de l’utilisateur dans un canal protégé.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 ou version ultérieure : la méthode est une méthode tunnelled et prend en charge le chaînage de méthodes EAP dans le tunnel.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 ou version ultérieure : la méthode prend en charge l’équivalence d’état partagé telle que définie dans la [norme RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Réservé. Non utilisé.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Clés de Registre pour les méthodes EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Constantes EAPHost communes](common-eap-host-error-constants.md)
</dt> </dl>

