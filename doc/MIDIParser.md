# Class: MIDIParser

## Table of contents

### Constructors

- [constructor](../wiki/MIDIParser#constructor)

### Properties

- [bytePointer](../wiki/MIDIParser#bytepointer)
- [data](../wiki/MIDIParser#data)
- [eventStartPointer](../wiki/MIDIParser#eventstartpointer)
- [fileDraft](../wiki/MIDIParser#filedraft)
- [runningStatus](../wiki/MIDIParser#runningstatus)
- [trackDraft](../wiki/MIDIParser#trackdraft)

### Methods

- [getChunkType](../wiki/MIDIParser#getchunktype)
- [nextByte](../wiki/MIDIParser#nextbyte)
- [nextWord](../wiki/MIDIParser#nextword)
- [parseChunk](../wiki/MIDIParser#parsechunk)
- [parseData](../wiki/MIDIParser#parsedata)
- [parseFile](../wiki/MIDIParser#parsefile)
- [read](../wiki/MIDIParser#read)
- [readVariableLengthQty](../wiki/MIDIParser#readvariablelengthqty)
- [parse](../wiki/MIDIParser#parse)

## Constructors

### constructor

• **new MIDIParser**()

#### Defined in

[midi-parser.ts:22](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L22)

## Properties

### bytePointer

• **bytePointer**: `number`

#### Defined in

[midi-parser.ts:13](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L13)

___

### data

• **data**: (``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``)[] = `[]`

#### Defined in

[midi-parser.ts:18](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L18)

___

### eventStartPointer

• **eventStartPointer**: `number`

While handling an event, this number should be set to the index of `data` pointing to the first byte of the current event's data, not including deltaTime

#### Defined in

[midi-parser.ts:17](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L17)

___

### fileDraft

• **fileDraft**: [`MidiFile`](../wiki/MidiFile)

#### Defined in

[midi-parser.ts:19](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L19)

___

### runningStatus

• **runningStatus**: ``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``

#### Defined in

[midi-parser.ts:21](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L21)

___

### trackDraft

• **trackDraft**: `MidiEvent`[] = `[]`

#### Defined in

[midi-parser.ts:20](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L20)

## Methods

### getChunkType

▸ `Private` **getChunkType**(): `ChunkType`

#### Returns

`ChunkType`

#### Defined in

[midi-parser.ts:107](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L107)

___

### nextByte

▸ **nextByte**(): ``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``

Read the next byte

#### Returns

``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``

#### Defined in

[midi-parser.ts:47](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L47)

___

### nextWord

▸ **nextWord**(`length?`): `number`

read the next n-byte word

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `length` | `number` | `2` |

#### Returns

`number`

#### Defined in

[midi-parser.ts:57](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L57)

___

### parseChunk

▸ `Private` **parseChunk**(): `void`

#### Returns

`void`

#### Defined in

[midi-parser.ts:118](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L118)

___

### parseData

▸ **parseData**(`data`): [`MidiFile`](../wiki/MidiFile)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Buffer` |

#### Returns

[`MidiFile`](../wiki/MidiFile)

#### Defined in

[midi-parser.ts:89](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L89)

___

### parseFile

▸ **parseFile**(`path`): `Promise`<[`MidiFile`](../wiki/MidiFile)\>

parse a MIDI file asynchronously, returning a promise that resolves to a MidiFile

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `string` |

#### Returns

`Promise`<[`MidiFile`](../wiki/MidiFile)\>

#### Defined in

[midi-parser.ts:84](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L84)

___

### read

▸ **read**(`length`): (``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``)[]

Read the next n bytes and return them as an array, advances the pointer

#### Parameters

| Name | Type |
| :------ | :------ |
| `length` | `number` |

#### Returns

(``0`` \| ``1`` \| ``2`` \| ``3`` \| ``4`` \| ``5`` \| ``6`` \| ``7`` \| ``8`` \| ``9`` \| ``10`` \| ``11`` \| ``12`` \| ``13`` \| ``14`` \| ``15`` \| ``16`` \| ``17`` \| ``18`` \| ``19`` \| ``20`` \| ``21`` \| ``22`` \| ``23`` \| ``24`` \| ``25`` \| ``26`` \| ``27`` \| ``28`` \| ``29`` \| ``30`` \| ``31`` \| ``32`` \| ``33`` \| ``34`` \| ``35`` \| ``36`` \| ``37`` \| ``38`` \| ``39`` \| ``40`` \| ``41`` \| ``42`` \| ``43`` \| ``44`` \| ``45`` \| ``46`` \| ``47`` \| ``48`` \| ``49`` \| ``50`` \| ``51`` \| ``52`` \| ``53`` \| ``54`` \| ``55`` \| ``56`` \| ``57`` \| ``58`` \| ``59`` \| ``60`` \| ``61`` \| ``62`` \| ``63`` \| ``64`` \| ``65`` \| ``66`` \| ``67`` \| ``68`` \| ``69`` \| ``70`` \| ``71`` \| ``72`` \| ``73`` \| ``74`` \| ``75`` \| ``76`` \| ``77`` \| ``78`` \| ``79`` \| ``80`` \| ``81`` \| ``82`` \| ``83`` \| ``84`` \| ``85`` \| ``86`` \| ``87`` \| ``88`` \| ``89`` \| ``90`` \| ``91`` \| ``92`` \| ``93`` \| ``94`` \| ``95`` \| ``96`` \| ``97`` \| ``98`` \| ``99`` \| ``100`` \| ``101`` \| ``102`` \| ``103`` \| ``104`` \| ``105`` \| ``106`` \| ``107`` \| ``108`` \| ``109`` \| ``110`` \| ``111`` \| ``112`` \| ``113`` \| ``114`` \| ``115`` \| ``116`` \| ``117`` \| ``118`` \| ``119`` \| ``120`` \| ``121`` \| ``122`` \| ``123`` \| ``124`` \| ``125`` \| ``126`` \| ``127`` \| ``128`` \| ``129`` \| ``130`` \| ``131`` \| ``132`` \| ``133`` \| ``134`` \| ``135`` \| ``136`` \| ``137`` \| ``138`` \| ``139`` \| ``140`` \| ``141`` \| ``142`` \| ``143`` \| ``144`` \| ``145`` \| ``146`` \| ``147`` \| ``148`` \| ``149`` \| ``150`` \| ``151`` \| ``152`` \| ``153`` \| ``154`` \| ``155`` \| ``156`` \| ``157`` \| ``158`` \| ``159`` \| ``160`` \| ``161`` \| ``162`` \| ``163`` \| ``164`` \| ``165`` \| ``166`` \| ``167`` \| ``168`` \| ``169`` \| ``170`` \| ``171`` \| ``172`` \| ``173`` \| ``174`` \| ``175`` \| ``176`` \| ``177`` \| ``178`` \| ``179`` \| ``180`` \| ``181`` \| ``182`` \| ``183`` \| ``184`` \| ``185`` \| ``186`` \| ``187`` \| ``188`` \| ``189`` \| ``190`` \| ``191`` \| ``192`` \| ``193`` \| ``194`` \| ``195`` \| ``196`` \| ``197`` \| ``198`` \| ``199`` \| ``200`` \| ``201`` \| ``202`` \| ``203`` \| ``204`` \| ``205`` \| ``206`` \| ``207`` \| ``208`` \| ``209`` \| ``210`` \| ``211`` \| ``212`` \| ``213`` \| ``214`` \| ``215`` \| ``216`` \| ``217`` \| ``218`` \| ``219`` \| ``220`` \| ``221`` \| ``222`` \| ``223`` \| ``224`` \| ``225`` \| ``226`` \| ``227`` \| ``228`` \| ``229`` \| ``230`` \| ``231`` \| ``232`` \| ``233`` \| ``234`` \| ``235`` \| ``236`` \| ``237`` \| ``238`` \| ``239`` \| ``240`` \| ``241`` \| ``242`` \| ``243`` \| ``244`` \| ``245`` \| ``246`` \| ``247`` \| ``248`` \| ``249`` \| ``250`` \| ``251`` \| ``252`` \| ``253`` \| ``254`` \| ``255``)[]

#### Defined in

[midi-parser.ts:36](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L36)

___

### readVariableLengthQty

▸ **readVariableLengthQty**(): `number`

Reads a variable length quantity

#### Returns

`number`

#### Defined in

[midi-parser.ts:66](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L66)

___

### parse

▸ `Static` **parse**(`file`): `Promise`<[`MidiFile`](../wiki/MidiFile)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `file` | `string` |

#### Returns

`Promise`<[`MidiFile`](../wiki/MidiFile)\>

#### Defined in

[midi-parser.ts:97](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L97)

▸ `Static` **parse**(`data`): [`MidiFile`](../wiki/MidiFile)

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Buffer` |

#### Returns

[`MidiFile`](../wiki/MidiFile)

#### Defined in

[midi-parser.ts:98](https://github.com/OscarLundberg/wave-function-collapse-mx/blob/9f12d93/src/midi-parser.ts#L98)