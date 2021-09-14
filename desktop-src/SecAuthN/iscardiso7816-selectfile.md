---
description: La méthode SelectFile construit une commande APDU (Application Protocol Data Unit) qui définit un fichier élémentaire actuel au sein d’un canal logique. Les commandes suivantes peuvent faire référence implicitement au fichier actif par le biais du canal logique.
ms.assetid: cb6231b3-fb1c-4350-8797-9efaa663c21b
title: 'ISCardISO7816 :: SelectFile, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SelectFile
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9bab499d32a65a2e6b4348458ec42328029760ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193947"
---
# <a name="iscardiso7816selectfile-method"></a>ISCardISO7816 :: SelectFile, méthode

\[La méthode **SelectFile** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **SelectFile** construit une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) qui définit un fichier élémentaire actuel au sein d’un canal logique. Les commandes suivantes peuvent faire référence implicitement au fichier actif par le biais du canal logique.

La sélection d’un répertoire (DF) dans le magasin de contenu de la carte, qui peut être la racine (MF) du cache de l’utilisateur, en fait le DF actuel. Après une telle sélection, un fichier élémentaire en cours implicite peut être référencé par ce canal logique.

La sélection d’un fichier élémentaire définit le fichier sélectionné et son parent en tant que fichiers actifs.

Après la réponse à la réinitialisation, le MF est implicitement sélectionné par le biais du canal logique de base, sauf s’il est spécifié différemment dans les octets historiques ou dans la chaîne de données initiale.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SelectFile(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in]      LONG         lBytesToRead,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*byP1* \[ dans\]
</dt> <dd>

Contrôle de sélection.



| P1 (octet supérieur dans Word) : 8 7 6 5 4 3 2 1                                                                                                                                                            | Signification                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span id="000000xx"></span><span id="000000XX"></span><dl> <dt>**000000xx**</dt><dt></dt> </dl> | Sélectionner l’ID de fichier<br/>          |
| <span id="00000000"></span><dl> <dt>**00000000**</dt><dt></dt> </dl>                            | EF, DF ou MF<br/>           |
| <span id="00000001"></span><dl> <dt>**00000001**</dt><dt></dt> </dl>                            | DF enfant<br/>                |
| <span id="00000010"></span><dl> <dt>**00000010**</dt><dt></dt> </dl>                            | EF sous DF<br/>             |
| <span id="00000011"></span><dl> <dt>**00000011**</dt><dt></dt> </dl>                            | DF parent du DF actuel<br/> |



 

Lorsque P1 = 00, la carte connaît soit en raison d’un codage spécifique de l’ID de fichier, soit en raison du contexte d’exécution de la commande si le fichier à sélectionner est MF, DF ou EF.

Lorsque P1-P2 = 0000, si un ID de fichier est fourni, il doit être unique dans les environnements suivants :

-   Enfants immédiats du DF actuel
-   DF parent
-   Enfants immédiats du DF parent

Si P1-P2 = 0000 et que le champ de données est vide ou égal à 3F00, sélectionnez le MF.

Lorsque P1 = 04, le champ de données est un nom DF, éventuellement tronqué à droite.

En cas de prise en charge, ces commandes successives avec le même champ de données doivent sélectionner DFs dont les noms correspondent à ceux du champ de données (autrement dit, commencez par le champ de données de la commande). Si la carte accepte la commande avec un champ de données vide, l’ensemble ou un sous-ensemble du DFs peut être sélectionné successivement.

</dd> <dt>

*byP2* \[ dans\]
</dt> <dd>

Contrôle de sélection.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Données pour l’opération si nécessaire ; Sinon, **null**. Les types de données passés dans ce paramètre sont les suivants :

-   ID de fichier
-   chemin d’accès à partir du MF
-   chemin du DF actuel
-   Nom du DF

</dd> <dt>

*lBytesToRead* \[ dans\]
</dt> <dd>

Vide (autrement dit, 0) ou longueur maximale des données attendues dans la réponse.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En entrée, pointeur vers un objet d’interface [**ISCardCmd**](iscardcmd.md) ou **null**.

Au retour, elle est remplie avec la commande APDU construite par cette opération. Si *ppCmd* a été défini avec la **valeur null**, un objet [**ISCardCmd**](iscardcmd.md) de [*carte à puce*](../secgloss/s-gly.md) est créé et retourné en interne par le biais du pointeur *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La méthode retourne l’une des valeurs possibles suivantes.



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Paramètre non valide.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Un pointeur incorrect a été passé.<br/>      |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

Sauf indication contraire, l’exécution correcte de la commande encapsulée modifie l’état de sécurité conformément aux règles suivantes :

-   Lorsque le fichier élémentaire actuel est modifié ou qu’il n’existe aucun fichier élémentaire en cours, l’état de sécurité spécifique à un ancien fichier élémentaire actuel est perdu.
-   Lorsque le répertoire de cache actuel (DF) est un descendant de ou identique à l’ancien DF actuel, l’état de sécurité spécifique à l’ancien DF actuel est perdu. L’état de sécurité commun à tous les ancêtres communs du DF précédent et du nouveau DF actuel est conservé.

Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardISO7816**](iscardiso7816.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Spécifications



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

 

 
