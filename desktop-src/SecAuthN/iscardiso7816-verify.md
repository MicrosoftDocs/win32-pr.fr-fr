---
description: Construit une commande APDU (Application Protocol Data Unit) qui initie la comparaison (dans la carte) des données de vérification envoyées à partir de l’appareil d’interface avec les données de référence stockées dans la carte (par exemple, le mot de passe).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816 :: Verify, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0d01fe47133ddeaf7bba32a91711d76783bdfbb0a28762d7ddb7f9054d0108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014439"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816 :: Verify, méthode

\[La méthode **verify** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **verify** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui initie la comparaison (dans la carte) des données de vérification envoyées à partir de l’appareil d’interface avec les données de référence stockées dans la carte (par exemple, le mot de passe).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byRefCtrl* \[ dans\]
</dt> <dd>

Quantificateur des données de référence. Le codage du contrôle de référence P2 suit.

Lorsque le corps est vide, la commande peut être utilisée pour récupérer le nombre « X » de nouvelles tentatives autorisées (SW1-SW2 = 63CX) ou pour vérifier si la vérification n’est pas requise (SW1-SW2 = 9000).



| Valeur                                                                                                                                                                                    | Signification                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Aucune information**</dt> </dl>                     | Position du bit : 00000000<br/> P2 = 00 est réservé pour indiquer qu’aucun qualificateur particulier n’est utilisé dans ces cartes où la commande Verify référence les données secrètes sans ambiguïté.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Référence globale**</dt> </dl>         | Position du bit : 0-------<br/> Un mot de passe est un exemple de référence globale.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Réf. spécifique**</dt> </dl> | Position du bit : 1-------<br/> Un mot de passe spécifique à DF est un exemple de référence spécifique.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Position du bit :-XX-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Données de référence \#**</dt> </dl>        | Position du bit :---xxxxx<br/> Le numéro de données de référence peut être, par exemple, un numéro de mot de passe ou un identificateur EF bref.<br/>                                                           |



 

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers les données de vérification. Ce paramètre peut être **NULL**. La valeur par défaut est **NULL**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini **sur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne à l’aide du pointeur *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | L’opération s’est terminée avec succès.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un paramètre non valide a été utilisé.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>            |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                          |



 

## <a name="remarks"></a>Remarques

L’état de sécurité peut être modifié à la suite d’une comparaison. Les comparaisons ayant échoué peuvent être enregistrées dans la carte (par exemple, pour limiter le nombre de tentatives supplémentaires d’utilisation des données de référence).

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                   |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 est défini en tant que 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
