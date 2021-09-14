---
description: L’interface ISCardISO7816 fournit des méthodes pour implémenter les fonctionnalités ISO 7816-4.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: Interface ISCardISO7816 (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 09e5dc9e84a36148e240e4ba2d31f04216454994
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193920"
---
# <a name="iscardiso7816-interface"></a>Interface ISCardISO7816

\[L’interface **ISCardISO7816** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. elle n’est pas disponible pour une utilisation dans Windows server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

L’interface **ISCardISO7816** fournit des méthodes pour implémenter les fonctionnalités ISO 7816-4. À l’exception de [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md), ces méthodes créent une commande APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) encapsulée dans un objet [**ISCardCmd**](iscardcmd.md) .

La spécification ISO 7816-4 définit les commandes standard disponibles sur les [*cartes à puce*](../secgloss/s-gly.md). La spécification définit également comment une commande APDU de carte à puce doit être construite et envoyée à la carte à puce pour être exécutée. Cette interface automatise le processus de création.

L’exemple suivant illustre une utilisation type de l’interface **ISCardISO7816** . Dans ce cas, l’interface **ISCardISO7816** est utilisée pour générer une commande APDU.

**Pour soumettre une transaction à une carte spécifique**

1.  Créez une interface **ISCardISO7816** et [**ISCardCmd**](iscardcmd.md) .

    L’interface [**ISCardCmd**](iscardcmd.md) est utilisée pour encapsuler le APDU.

2.  Appelez la méthode appropriée de l’interface **ISCardISO7816** , en passant les paramètres requis et le pointeur d’interface [**ISCardCmd**](iscardcmd.md) .

    La commande ISO 7816-4 APDU sera générée et encapsulée dans l’interface [**ISCardCmd**](iscardcmd.md) .

3.  Libérez les interfaces **ISCardISO7816** et [**ISCardCmd**](iscardcmd.md) .

> [!Note]  
> Dans les pages de référence de méthode, si une séquence de bits dans une table n’est pas définie, supposez que la séquence de bits est réservée à un usage ultérieur ou propriétaire d’un fournisseur spécifique.

 

## <a name="members"></a>Membres

L’interface **ISCardISO7816** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardISO7816** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISCardISO7816** possède ces méthodes.



| Méthode                                                             | Description                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Construit une commande qui ajoute un enregistrement à la fin d’un fichier élémentaire (EF).<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Définit une partie du contenu d’un EF à son état logique effacé, de manière séquentielle, à partir d’un offset donné.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Met à jour de manière conditionnelle l’état de sécurité à l’aide du résultat du calcul par la carte, en fonction d’une demande précédemment émise par la carte (par exemple, par la \_ commande ins obtenir \_ un Challenge), d’une clé secrète éventuellement stockée dans la carte et des données d’authentification transmises par l’appareil d’interface.<br/> |
| [**GetChallenge**](iscardiso7816-getchallenge.md)                 | Requiert l’émission d’un défi à utiliser dans le cas d’une procédure liée à la sécurité.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Récupère un objet de données primitif unique ou un ensemble d’objets de données contenus dans un objet de données construit, en fonction du type de fichier spécifié.<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | Transmet de la carte aux unités APDU de l’interface qui, autrement, ne peuvent pas être transmises par les protocoles disponibles.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Lance le calcul des données d’authentification par la carte à l’aide des données de stimulation envoyées à partir de l’appareil d’interface et d’une clé secrète appropriée stockée dans la carte.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Ouvre et ferme des canaux logiques.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Stocke un objet de données primitif, ou un ou plusieurs objets de données contenus dans un objet de données construit, dans le [*contexte du gestionnaire de ressources*](../secgloss/r-gly.md)actuel.<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Construit une commande qui acquiert un message de réponse qui donne la partie du contenu d’un EF avec une structure transparente.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Construit une commande qui lit le contenu des enregistrements spécifiés d’un fichier élémentaire.<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | Définit un fichier actif dans un canal logique.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Affecte un octet d’ID de classe standard qui sera utilisé dans toutes les opérations lors de la construction d’une commande ISO 7816-4.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Lance la mise à jour des bits déjà présents dans un EF avec les bits fournis dans la commande APDU.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Construit une commande qui lance la mise à jour d’un enregistrement spécifique.<br/>                                                                                                                                                                                                                                  |
| [**Vérification**](iscardiso7816-verify.md)                             | Lance la comparaison de la carte des données de vérification envoyées à partir de l’appareil d’interface avec les données de référence stockées dans la carte.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Initie l’écriture de valeurs binaires dans un EF.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Construit une commande qui écrit un enregistrement.<br/>                                                                                                                                                                                                                                                              |



 

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



 

 
